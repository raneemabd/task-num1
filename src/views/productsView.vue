<template>
    <section style="background-color: #fcffe7">
      <h1 class="text-center  py-8" style="color: #603e1b">Wear Good, Be Good!</h1>
    
      <v-container>
  
        <v-row >
          <v-col
            cols="12"
            sm="6"
            md="6"
            lg="4"
            xl="3"
            v-for="product in products"
            :key="product.id"
          >
          <v-hover v-slot="{ isHovering, props }" open-delay="200">
        
        <v-card 
          :elevation="isHovering ? 16 : 2"
          :class="{ 'on-hover': isHovering }"
          class="mx-auto "
          max-width="550"
          v-bind="props">
          <v-img :src="product.image" height="200px" cover></v-img>
          <v-card-title>{{ product.title }}</v-card-title>
          <v-card-text>{{ product.category }} </v-card-text>
          <v-divider></v-divider>
          <v-card-text><b>Price: </b> {{ product.price }} $</v-card-text>
          <v-card-actions>
            <v-btn
              variant="tonal"
              color="#5F8D3E"
             
              >Add To <v-icon class="ml-2"> mdi-cart </v-icon>
              <v-overlay
                activator="parent"
                location-strategy="connected"
                scroll-strategy="reposition"
              >
                <v-card class="pa-2" color="primary">
                  Successfuly Added , Lets Add More !
                </v-card>
              </v-overlay>
            </v-btn>
            <v-btn
              variant="tonal"
              color="#ff0000"
              :to="url"
              >
    
              Details
            </v-btn>
            <v-spacer></v-spacer>
            <v-btn to="/likes"> <v-icon color="red"> mdi-heart </v-icon></v-btn>
    
            <v-btn
              :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'"
              @click="show = !show"
            ></v-btn>
          </v-card-actions>
          <v-expand-transition>
            <div v-show="show">
              <v-divider></v-divider>
              <v-card-text>{{ product.description }} </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </v-hover>
          </v-col>
        </v-row>
        
      </v-container>
    </section>
  
    <v-divider></v-divider>
   
    
  </template>
  
  <script>
  
 

import products from "@/store/products";

import { mapActions, mapState } from "pinia";
  export default {


    computed: {
  ...mapState(products, ["products"]),
  
},

methods: {
    
    
  },
}
  </script>
  