<template>
      <v-app-bar color="primary">
    <v-app-bar-title class="red--text text--lighten-1">
      <v-btn to="/likes" stacked>
        <v-icon color="#fcffe7"> mdi-cart </v-icon>
      </v-btn>

    </v-app-bar-title>

    <template #append>
      <v-btn color="#fcffe7" to="/" exact stacked> Home </v-btn>

      <v-btn color="#fcffe7 darken-3" to="/products" stacked> Products </v-btn>
      <v-btn color="#fcffe7 darken-3" to="/Contact" stacked>Contact Us  </v-btn>
     
    
    </template>
  </v-app-bar>
</template>