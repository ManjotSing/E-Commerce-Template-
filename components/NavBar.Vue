<template>
    <div>
        <b-navbar toggleable="lg" type="dark" variant="success">
            <b-navbar-brand @click="goHome" href="#">
                <b-icon-brighness-high-fill>
                </b-icon-brighness-high-fill>
                E-Commerce
            </b-navbar-brand>
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
