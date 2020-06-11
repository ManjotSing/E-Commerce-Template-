<template>
    <div >
        <b-navbar toggleable="lg" type="light" variant="info">
            <b-navbar-brand @click="goHome" href="#" >
                 <img src='Khelo Lottery.png' alt="Khelo" width="70" height = "60">
            </b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
             <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav>
                     <!-- Navbar dropdowns -->
                     <b-nav-item href="#" class="m-md-1">Home</b-nav-item>
                     <b-nav-item href="#" class="m-md-1">Daily Lottery2020</b-nav-item>
                     <b-nav-item href="#" class="m-md-1">Recent Winners</b-nav-item>
                     <b-nav-item-dropdown text="Punjab State Lotteries"  class="m-md-1" left>
                            <b-dropdown-item href="#">Latest Lottery Schemes</b-dropdown-item>
                            <b-dropdown-item href="#">Sikkim State Lotteries</b-dropdown-item>
                            <b-dropdown-item href="#">Nagaland State Lotteries</b-dropdown-item>
                     </b-nav-item-dropdown>
                     <b-nav-item-dropdown text="Results"  class="m-md-1" left>
                            <b-dropdown-item href="#">Nagaland Daily Results</b-dropdown-item>
                            <b-dropdown-item href="#">Sikkim Daily Results</b-dropdown-item>
                            <b-dropdown-item href="#">Goa State Rajshree Results</b-dropdown-item>
                            <b-dropdown-item href="#">Order</b-dropdown-item>
                      </b-nav-item-dropdown>
                </b-navbar-nav>

             </b-collapse>
             </b-navbar-toggle>
 
       <!-- <b-nav-item-dropdown text="Lang" left>
          <b-dropdown-item href="#">EN</b-dropdown-item>
          <b-dropdown-item href="#">ES</b-dropdown-item>
          <b-dropdown-item href="#">RU</b-dropdown-item>
          <b-dropdown-item href="#">FA</b-dropdown-item>
        </b-nav-item-dropdown> -->
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>  
            <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav class = "ml-auto">
                    <b-nav-item @click="gotocart" active>Shopping Cart </b-nav-item>
                        <b-nav-item-dropdown right>
                            <template v-slot:button-context>
                                <em>Admin</em>
                            </template>
                            <b-dropdown-item v-b-modal.modal-1>Sign In</b-dropdown-item>
                        </b-nav-item-dropdown>
                </b-navbar-nav>
            </b-collapse>  
        </b-navbar>

    <div>
    <b-modal hide-footer ref="my-modal" id="modal-1" title="Admin">
        <b-from @submit= "onSubmit">
            <b-form-group
                id=input-group-1
                label="User:"
                label-for="input-1"
                >
                <b-form-input
                    id= "input-1"
                    type="text"
                    required
                    placeholder="Enter User">
                </b-form-input>
            </b-form-group>
            <b-form-group id ="input-group-2" label = "Password" label-for="input-2">
                <b-form-input
                    id= "input-2"
                    type="password"
                    required
                    placeholder="Enter Password">
                </b-form-input>
            </b-form-group>
        <b-button type="submit" blovk variant="primary"> 
            Submit
        </b-button>
        </b-from>
    </b-modal>
    </div>
    </div>
</template>
