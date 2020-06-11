<template>
    <div class="conatiner">
        <b-carousel 
        id="carousel-1"
        v-model="slide"
        :interval="3000"
        controls
        indicators
        background="#ababab"
        img-width="960"
        img-height="480"
        style="text-shadow: 1px 1px 2px #333;"
        >
        <b-carousel-slide>
            <template v-slot:img>
                <img
                 class = "d-block img-fluid w-100"
                 style = "height:80vh!important;"
                 :src="require('@/assets/img/wall1.png')"
                 alt="image slot" 
                >
            </template>
        </b-carousel-slide>
        <b-carousel-slide>
            <template v-slot:img>
                <img
                 class = "d-block img-fluid w-100"
                 style = "height:80vh!important;"
                 :src="require('@/assets/img/wall3.png')"
                 alt="image slot"
                
                >
            </template>
        </b-carousel-slide>
        <b-carousel-slide>
            <template v-slot:img>
                <img
                 class = "d-block img-fluid w-100"
                 style = "height:80vh!important;"
                 :src="require('@/assets/img/wall2.png')"
                 alt="image slot"
                >
            </template>
        </b-carousel-slide>
        </b-carousel>
    </div>
</template>
<script>
export default{
    data() {
        return{
            slide : 0,
            sliding : null
        }
    },
    methods: {

    }
}
</script>