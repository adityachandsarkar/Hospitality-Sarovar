<template>
<div
class= "typeface">
<v-container class="grey lighten-5">
    <v-row>
    <!--offset defines position/distance between image and text-->
      <v-col
        md="6" 
        offset-md="3"
        <img
        class="offer"
        alt="offer"
        <v-img
        src="https://www.islamabadscene.com/wp-content/uploads/2018/02/Hotel-Sale-deal.jpg"
        class="rounded-xl">
        </v-img>
        </v-col>

   
      <v-col
        cols="12"
        md="4" 
        ><!--text body-->
         <h1>Special Offers</h1>
         <h2 class="text--disabled">--------------------------</h2>
         <h3>Long Weekend Sale</h3>
         <h6 class="text--disabled">--------------------------</h6>
         <p class="text-lg-left">We welcome our guests to experience the essence of life with our personalised services, warm hospitality, and seamless facilities. Immerse yourself in a wealth of enriching experiences, and have a beautiful and hassle-free stay that you would cherish forever.
                                 Come, discover the refreshing signature experience across 3 great Sarovar brands.
        </p>
        
      </v-col>
      
    </v-row>
  </v-container>
  </div>
</template>
<style>
.offer {
  height: 500px;
  width: 700px;
  margin-left: 0px;
  }
.typeface {
  font-family: "poppins";
}  
</style>
