<template>
  <div class="Team">
  <h1 class="subheading grey--text">Products</h1>

  <v-container class="my-5">
    
    <!-- <v-slide-item>
    <v-layout row wrap>
      <v-flex xs12 sm6 md4 lg3 v-for="team in teams" :key="team.name">
        
        <v-card flat class="text-center ma-4 ">
  
           <v-reponstive class="pt-4">
            <v-avatar>
              <img :src="team.image">
            </v-avatar>
          </v-reponstive>
          <v-card-text>
            <div class="subheading">{{team.name}}</div>
            <div class="grey--text">{{team.description}}</div>
          </v-card-text>  
           
        </v-card>
      </v-flex>
    </v-layout>
  </v-slide-item>-->
  <v-sheet
    class="mx-auto"
    elevation="8"
    width="100%"
  >
    <v-slide-group
      v-model="model"
      class="pa-4"
      active-class="success"
      show-arrows
    >
      <v-slide-item
        v-for="team in teams" :key="team.name"
        v-slot="{ active, toggle }"
      >
        <v-card
          :color="active ? undefined : 'white lighten-1'"
          class="text-center ma-4"
          @click="toggle"
        >
          <!-- <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <v-scale-transition>
              <v-icon
                v-if="active"
                color="white"
                size="48"
                v-text="'mdi-close-circle-outline'"
              ></v-icon>
            </v-scale-transition>
          </v-row> -->
          <v-reponstive class="pt-5">
           <img height="150" :src="team.image">
          </v-reponstive>
           <v-divider class="mx-4"></v-divider> 
          <v-card-text>
           <div class="black--text" light>{{team.name}}</div>
          <div class="grey--text">{{team.description}}</div>
          </v-card-text> 
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
</v-container> 
<v-container>
  <v-sheet
    class="mx-auto"
    elevation="8"
    width="100%"
  >
    <v-slide-group
      v-model="model"
      class="pa-4"
      active-class="success"
      show-arrows
    >
      <v-slide-item
        v-for="product in products" :key="product.name"
        v-slot="{ active, toggle }"
      >
        <v-card
          :color="active ? undefined : 'white lighten-1'"
          class="text-center ma-4"
          @click="toggle"
        >
          <!-- <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <v-scale-transition>
              <v-icon
                v-if="active"
                color="white"
                size="48"
                v-text="'mdi-close-circle-outline'"
              ></v-icon>
            </v-scale-transition>
          </v-row> -->
          <v-reponstive class="pt-5">
           <img height="150" :src="product.image">
          </v-reponstive> 
          <v-card-text>
           <div class="black--text" light>{{product.name}}</div>
           <v-divider class="mx-4"></v-divider>

            <div class="grey--text">{{product.description}}</div>
          </v-card-text> 
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
  </v-container>
  </div>

</template>

<script>

export default {
  data(){
    return{
      teams : [
        {name : 'Product Name',description:'Product Description',image:'/index3.jpg' },
        {name : 'Products',description:'Product Description',image:'/index3.jpg' },
        {name : 'Product Category',description:'Product Description',image:'/index3.jpg' },
        {name : 'Product sub Category',description:'Product Description',image:'/index3.jpg' },
        {name : 'Product Description',description:'Product Description',image:'/index3.jpg' },
         {name : 'Product Name',description:'Product Description',image:'/index3.jpg' },
        {name : 'Products',description:'Product Description',image:'/index3.jpg' },
        {name : 'Product Category',description:'Product Description',image:'/index3.jpg' },
        {name : 'Product sub Category',description:'Product Description',image:'/index3.jpg' },
        {name : 'Product Description',description:'Product Description',image:'/index3.jpg' },
      ],

      products :[
         {name : 'Product Name',description:'Product Description',image:'/index4.jpg' },
        {name : 'Products',description:'Product Description',image:'/index4.jpg' },
        {name : 'Product Category',description:'Product Description',image:'/index4.jpg' },
        {name : 'Product sub Category',description:'Product Description',image:'/index4.jpg' },
        {name : 'Product Description',description:'Product Description',image:'/index4.jpg' },
         {name : 'Product Name',description:'Product Description',image:'/index4.jpg' },
        {name : 'Products',description:'Product Description',image:'/index4.jpg' },
        {name : 'Product Category',description:'Product Description',image:'/index4.jpg' },
        {name : 'Product sub Category',description:'Product Description',image:'/index4.jpg' },
        {name : 'Product Description',description:'Product Description',image:'/index4.jpg' },
      ]
    }
  }
}
</script>
