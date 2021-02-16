<template>
    <nav>
        <v-toolbar app >
              <v-app-bar-nav-icon class="grey--text" @click.stop="drawer = !drawer"><v-icon right>mdi-menu</v-icon></v-app-bar-nav-icon>  
            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light">ad</span>
                <span>Flash</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
             <v-col
          cols="12"
          sm="6"
          md="3"
        >
            <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        hide-details
      ></v-text-field>
             </v-col>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
            <v-btn color="grey" dark>
            <span>Sign Out</span>
            <v-icon right>logout</v-icon>
            </v-btn>
        </v-toolbar>

        <v-navigation-drawer v-model="drawer" absolute bottom temporary class="primary">
            <v-list>
            <v-list-item-group>
                <v-list-item v-for="link in links" :key="link.text" router  :to= "link.route">
                <v-list-item-icon>
                    <v-icon class="white-text" dark>{{ link.icon}}</v-icon>
                </v-list-item-icon>
                <v-list-item-content> 
                    <v-list-item-title class="white--text">{{ link.text}}</v-list-item-title>
                </v-list-item-content>
                </v-list-item>
            </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>
<script>
export default {
    data(){
        return{
            drawer:false,
            links : [
                {icon : 'dashboard', text :'Dashboard', route : '/'},
                 {icon : 'folder', text :'My Projects', route : '/projects'},
                  {icon : 'person', text :'Team', route : '/team'},
            ]
        }
    }
    
}
</script>