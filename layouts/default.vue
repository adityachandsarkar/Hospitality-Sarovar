<template>
  <!--Your App Starts Here -->
  <v-app id="inspire">
    
    <!--Header -->
    <v-app-bar color="white" dark fixed app>
      <v-toolbar-title></v-toolbar-title>
       <!-- Component Example -->
      <blog/>
      <question/>
      <sarlogo/>
      <signin/>
      
    </v-app-bar>

    <!-- Body -->
    <v-content light>
      <nuxt /> 
    </v-content>
    
    <!-- Footer -->
    <v-footer color="indigo" app>
      <span class="white--text">&copy; {{ new Date().getFullYear() }}</span>
      <v-row>
      <p>Lorem ipsum</p>
      </v-row>    
    </v-footer>

  </v-app>
</template>

<script>
export default {}
</script>

<style> 
  .white--text {
    border: 1px solid;
  }

   #inspire {
    background-color: lightblue;
    color: black;
  }
</style>