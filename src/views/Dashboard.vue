<template>
  <div class="Dashboard">
  <h1 class="subheading grey--text" >Dashboard</h1>

   <v-container class="my-5">
    <v-card flat class="pa-3" v-for="project in projects" :key="project.title">
      <v-layout row wrap :class="'pa-4 project ${project.status}'">
        <v-flex xs12 md6>
          <div class="caption grey--text">Project title</div>
          <div>{{project.title}}</div>
        </v-flex>
        <v-flex xs6 sm4 md2>
          <div class="caption grey--text">Person</div>
          <div> {{project.person}} </div>
        </v-flex> 
         <v-flex xs6 sm4 md2>
          <div class="caption grey--text">Due by</div>
          <div>{{project.due}}</div>
        </v-flex> 
         <v-flex xs2 sm4 md2>
          <!-- <div class="caption grey--text">Status</div>
          <div>{{project.status}}</div> -->
          <v-chip small class="ma-2 white--text" color="primary">{{project.status}}</v-chip>
        </v-flex> 
      </v-layout>
      <v-divider></v-divider>
    </v-card>
  </v-container>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  data(){
    return{
      projects: [
        {title : 'Design', person : 'text New hello', due : "1st",status:'complete'},
        {title : 'Design1', person : 'text  hello', due : "2nd",status:'complete'},
        {title : 'Design2', person : ' New hello', due : "3rd",status:'complete'},
        {title : 'Design3', person : 'text New ', due : "4th",status:'complete'},
        {title : 'Design4', person : ' hello', due : "5th",status:'complete'}
      ]
    }
  }
}
</script>
<style>
.project.complete{
border-left: 4px solid #3cd1c2;
}

.v-chip.complete{
  background:#3cd1c2 ;
}
</style>