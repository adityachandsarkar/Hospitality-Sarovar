<template>
  <!--Your App Starts Here -->
  <v-app id="inspire">
    
    <!--Header -->
    <v-app-bar color="white" light fixed app>
      <v-toolbar-title></v-toolbar-title>
       <!-- Component Example -->
      <blog/>
      <sarlogo/>
      <signin/>
      
    </v-app-bar>

    <!-- Body -->
    <v-content light>
      <nuxt /> 
    </v-content>
    
    <!-- Footer -->
   
  
         
    

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
    background-color: white;
    color: black;
  }
</style>