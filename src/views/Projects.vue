<template>
  <div class="Projects">
  <h1 class="subheading grey--text">Projects</h1>

   <v-container class="my-5">
    <v-layout row wrap>
      <v-flex xs12 sm6 md4 lg3 v-for="team in teams" :key="team.name">
        
        <v-card flat class="text-center ma-4 ">
  
           <v-reponstive class="pt-4">
            
              <img  height="150" :src="team.image">
            
          </v-reponstive>
           <v-divider class="mx-4"></v-divider>
           <v-card-title primary-title class="justify-center">{{team.name}}</v-card-title>
          <v-card-text>
            <!-- <div class="subheading">{{team.name}}</div> -->
            <div class="grey--text">{{team.description}}</div>
          </v-card-text>  
           
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
   data(){
    return{
         teams : [
        {name : 'Product Name',description:'Product Description',image:'/index3.jpg' },
        {name : 'Products',description:'Product Description',image:'/index4.jpg' },
        {name : 'Product Category',description:'Product Description',image:'/index3.jpg' },
        {name : 'Product sub Category',description:'Product Description',image:'/index4.jpg' },
        {name : 'Product Description',description:'Product Description',image:'/index3.jpg' },
         {name : 'Product Name',description:'Product Description',image:'/index4.jpg' },
        {name : 'Products',description:'Product Description',image:'/index3.jpg' },
        {name : 'Product Category',description:'Product Description',image:'/index4.jpg' },
        {name : 'Product sub Category',description:'Product Description',image:'/index3.jpg' },
        {name : 'Product Description',description:'Product Description',image:'/index4.jpg' },
      ]
    }
  }
}
</script>
