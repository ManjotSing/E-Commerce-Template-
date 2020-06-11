<template>
<div class = "container">
    <b-container fluid class="bv-example-row mt-4">
        <b-row>
            <b-col cols="3" v-for="(lottery,index) in lotteries" :key="index">
                <b-card
                :title = lottery.name
                :img-src="require(`@/assets/lottery/lottery${index+1}.png`)"
                img-alt = "Image" 
                img-top
                tag="article"
                class="mb-4">

                <b-card-text>
                    <h5>Price: ${{lottery.price}}.00</h5>
                    <b-icon variant="warning" class="h1" icon="star-fill"></b-icon>
                    <b-icon variant="warning" class="h1" icon="star-fill"></b-icon>
                    <b-icon variant="warning" class="h1" icon="star-fill"></b-icon>
                    <b-icon variant="warning" class="h1" icon="star-fill"></b-icon>
                    <b-icon variant="warning" class="h1" icon="star-fill"></b-icon>
                </b-card-text>

                <b-button v-if="!lottery.cart" :disabled="lottery.cart" @click="lottery.cart=true,
                addToCart(JSON.parse(JSON.stringify(lottery)))"  block href="#" variant="success">Add to Cart</b-button>
                <b-button v-if="lottery.cart" :disabled="lottery.cart" block href = "#"
                 variant="success">Already added to shopping cart</b-button>
                </b-card>
            </b-col>
        </b-row>
    </b-container>
</div>
</template>

<script>
    export default{
        data() {
            return {
                lotteries:[
                    {
                        id:1,
                        quantity:1,
                        name:"Atlanta",
                        price:1,
                        img:'/@assets/img/wall1.png',
                        cart:false
                    },
                    {
                        id:2,
                        quantity:1,
                        name:"Bulgaria",
                        price:1,
                        img:'/@assets/img/wall2.png',
                        cart:false
                    },
                    {
                        id:3,
                        quantity:1,
                        name:"Hongkong",
                        price:1,
                        img:'/@assets/img/wall3.png',
                        cart:false
                    },
                    {
                        id:4,
                        quantity:1,
                        name:"Japan",
                        price:1,
                        img:'/@assets/img/wall3.png',
                        cart:false
                    },
                    {
                        id:5,
                        quantity:1,
                        name:"USA",
                        price:1,
                        img:'/@assets/img/wall3.png',
                        cart:false
                    },
                    {
                        id:6,
                        quantity:1,
                        name:"Phillipnes",
                        price:1,
                        img:'/@assets/img/wall3.png',
                        cart:false
                    },
                    {
                        id:7,
                        quantity:1,
                        name:"Canada",
                        price:1,
                        img:'/@assets/img/wall3.png',
                        cart:false
                    },
                    {
                        id:8,
                        quantity:1,
                        name:"UK",
                        price:1,
                        img:'/@assets/img/wall3.png',
                        cart:false
                    }
                    
  
                ]
            }
        },
        methods: {
            addToCart(lottery){
                let cart=[]
                if(JSON.parse(localStorage.getItem('lotteries'))){
                    cart = JSON.parse(localStorage.getItem('lotteries'))
                }else{
                    cart = []
                }
                cart.push(lottery);
                localStorage.setItem('lotteries',JSON.stringify(cart))
            },
            created(){
                let cart = []
                if(JSON.parse(localStorage.getItem('lotteries'))){
                    cart = JSON.parse(localStorage.getItem('lotteries'))
                }else{
                    cart = []
                }
                for(let index =0;index<cart.length;index++){
                    for(let index2 =0;index2<this.lotteries.length;index2++){
                        if(cart[index].id == this.lotteries[index2].id){
                            this.lotteries[index2]== true
                        }
                    }
                }

            }
        }
    }
</script>