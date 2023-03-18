<template>
    <section style="background-color: #b4cfa0e5">
    <v-container >
      <h1 class="font-weight-bold my-10 text-center pb-6 text-primary" >
        What Are You Looking For ?
      </h1>
      <v-row>
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card class="mx-auto" max-width="344"      >
            <v-img
              src="@/assets/women.jpg"
              height="200px"
              cover
            ></v-img>
            <v-card-title > Women's Collection </v-card-title>
        
            <v-card-actions>
              <v-btn color="orange-lighten-2" to="/products/women"> Shop Now </v-btn>
              <v-spacer></v-spacer>
            </v-card-actions>
            <v-expand-transition>
              <div>
                <v-divider></v-divider>
                <v-card-text 
                  >Improving lives through clothes by suppoting families that need it most. Wear Good Be Good.
                  fashion clothes for women. dress clothes for women.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card class="mx-auto" max-width="344"         >
            <v-img src="@/assets/men.jpg" height="200px" cover></v-img>
            <v-card-title > Men's Collection </v-card-title>
            
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" to="/products/men"> Shop Now </v-btn>
            
              <v-spacer></v-spacer>
            </v-card-actions>
            <v-expand-transition>
              <div>
                <v-divider></v-divider>
                <v-card-text >
                  Discover the latest trends in men's fashion and style with us.
                  For an amazing men's clothing store or men's clothing online.
                  Find the trendiest clothes for Men.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>

  <section class="py-10" style="background-color:  #FCFFE7;">
    <v-container >
      <h1 class="font-weight-bold my-10 text-center pb-6 text-primary" >
        <b>Chek Out Our New Offers!</b>
        <div class="animation">
          <v-icon  color="#5f8d3e">
            mdi-chevron-double-down
          </v-icon>
        </div>
      </h1>
      <v-carousel hide-delimiters cycle id="carousel" show-arrows="hover">
        

        <v-carousel-item
          src="../../offer1.jpg"
          cover class="scale"
         style="width: 100%;"
        ></v-carousel-item>



        <v-carousel-item
          src="../../offer2.jpg"
          cover class="scale"
        ></v-carousel-item>
       

      </v-carousel>
      
    </v-container>
  </section>

</template>

<style>

.scale{
  animation: scale 6s infinite;
}
@keyframes scale {
  from{
    transform: scale(1);
  }
  to{
    transform: scale(1.4);
  }
}
.animation{
  animation: tran 1s ease-in-out alternate infinite ;
}
@keyframes tran{
    to{
        transform: translateY(20px);
    }
}
#carousel{
  width: 90%;
 margin: 0 auto;
  border-radius: 1%;
  box-shadow: 0px 10px 10px #80663f;
}
h1{
  font-family: "Brush Script MT", cursive;
  font-size: 36px;

}

</style>