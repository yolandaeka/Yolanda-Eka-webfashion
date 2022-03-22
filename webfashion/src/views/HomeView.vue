<template>
 <div class="home">

  <v-carousel hide-delimiters
  height="465">
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    >


    <v-row  
    align="center"
    justify="center"
    style="height: 470px;"
    no-gutters
    wrap>

    <v-card
    color="transparent"
    elevation="0"
    align="center"
    >

    <v-card-text class="series-change white--text text-center">Elizabeth Series</v-card-text>
    
    <v-btn 
    class= "btn-change white--text "
        color="#D9B285"
        elevation="3"
    >  SEE COLLECTION 
    </v-btn>
    
        </v-card>
      </v-row>
    </v-carousel-item>
  </v-carousel>

  <v-spacer></v-spacer>

  <!-- latest section -->

<v-container >
   <v-card-title class="title-card"> LATEST
    <v-spacer></v-spacer>
    <v-btn
    text
    class="black--text">
        SEE ALL
      </v-btn>
  </v-card-title>
  
  
  <v-row
    align="center"
    justify="center"
    >
    <v-col
      v-for="(product,i) in products"
      :key="i"
      >

  <v-card
    max-width="216"
    class="mx-auto"
    justify="center"
    
  >

    <v-img
      :src="product.image" width="216" height="320"
    ></v-img>

    <v-card-title class="card-latest">{{product.name}}</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          4.5 (413)
        </div>
      </v-row>
    
    </v-card-text>

      <v-card-text color="#EB801E" class="price" >
          {{ product.price }}
        </v-card-text>

      <v-spacer></v-spacer>

    <v-card-actions>
      <v-btn
      
        color="#D9B285"
        @click="reserve"
        class="white--text mt-5"
        block
        elevation="5"
      >
       ADD TO CART
      </v-btn>
    </v-card-actions>
  </v-card>

</v-col>
  </v-row>
</v-container>

<v-spacer></v-spacer>
  

  <!-- POPULAR SECTION -->
<v-container  mb-10>
  <v-card-title class="title-card">POPULAR
    <v-spacer></v-spacer>
    <v-btn
    text
    class="black--text">
        SEE ALL
      </v-btn>
  </v-card-title>

  <v-row
    align="center"
    justify="center"
    >
    <v-col
      v-for="(product,i) in products"
      :key="i"
      >

  <v-card
    max-width="216"
    class="mx-auto"
    justify="center"
    
  >

    <v-img
      :src="product.image" width="216" height="320"
    ></v-img>

    <v-card-title class="card-latest">{{product.name}}</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          4.5 (413)
        </div>
      </v-row>
    
    </v-card-text>

      <v-card-text color="#EB801E" class="price" >
          {{ product.price }}
        </v-card-text>

      <!-- <v-spacer></v-spacer> -->

    <v-card-actions>
      <v-btn
      
        color="#D9B285"
        @click="reserve"
        class="white--text mt-5"
        block
        elevation="5"
      >
       ADD TO CART
      </v-btn>
    </v-card-actions>
  </v-card>

</v-col>
  </v-row>
  
  </v-container>


  <!-- ABOUT SECTION -->

<v-spacer></v-spacer>

  <v-row 
  class="mt-5 mb-5"
    no-gutters
    style="height: 437px;"
    justify
    >
    <v-col>

  <v-img
   src="../assets/imghome/image 4.png">

 <v-card
    color="transparent"
    elevation="0"
    align="center"
    >

    <v-card-text class="about white--text" width="100" height="144" >Lorem ipsum dolor sit amet, 
      consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna 
      aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip 
      ex ea commodo consequat. Duis aute irure dolor in reprehenderit in 
      voluptate velit esse cillum dolore eu fugiat nulla pariatur.</v-card-text>
    
    <v-btn 
    class= "btn-change white--text "
        color="#D9B285"
        elevation="3"
    >  SEE COLLECTION 
    </v-btn>
    
    </v-card>
  </v-img>
  </v-col>
</v-row>


<!-- rating section -->

<v-container>

  <v-card-title class="title-card text-center justify-center"> TESTIMONIALS</v-card-title>
  <v-row>
    

    <v-col>
      <v-card
    max-width="374"
  >
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img
      height="250"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
    ></v-img>

    <v-card-title>Cafe Badilico</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          4.5 (413)
        </div>
      </v-row>
      </v-card-text>
   
  </v-card>








    </v-col>






  </v-row>




</v-container>


</div>
</template>



<script>

// eslint-disable-next-line no-unused-vars


export default {
  
    data () {
      return {
      items: [
        {
          src: require('../assets/imghome/webphoto (1).png')
        },
        {
          src: require('../assets/imghome/webphoto (2).png')
        },
        {
          src: require('../assets/imghome/webphoto (3).png')
        }
      ],

      products: [
        {
        image: "https://i.pinimg.com/564x/99/12/22/991222ca391c945718feab5ffa47f359.jpg",
        name : "Green Plaid Long Skirt from Elizabeth Series",
        price : "Rp 150.000"

        },

        {

        image: "https://i.pinimg.com/564x/24/f7/af/24f7affc7e3c13e2e498fc3c63dc1f49.jpg",
        name : "Green Plaid Long Skirt from Elizabeth Series",
        price : "Rp 160.000"
        },

        {
        image: "https://i.pinimg.com/564x/f1/d7/e6/f1d7e6be9189157868fe81507a3e90b5.jpg",
        name : "Green Plaid Long Skirt from Elizabeth Series",
        price : "Rp 90.000"
        },

        {
        image: "https://i.pinimg.com/564x/67/21/3c/67213c8f543a2081c2ff3bd69c02beb3.jpg",
        name : "Green Plaid Long Skirt from Elizabeth Series",
        price : "Rp 250.000"

        }

      ]



      }
    }
}
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@700&family=Montserrat:wght@500;600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap');

.btn-change{
  font-family:'Montserrat', sans-serif;
  font-size: 14px;
}

.series-change{
   font-family: 'Merriweather',serif;
   font-size: 22px;
   letter-spacing: 5px;
   font-weight: 700;
}


.title-card{
  font-family:'Montserrat', sans-serif;
  font-weight: 700;
  font-size: 20px;


}

.card-latest{
  font-family: 'Merriweather',serif;
   font-size: 13px;
   line-height: 24px;
  
}

.price{
  font-size: 17px
}

.about{
    font-family:'Montserrat', sans-serif;
  font-weight:500;
  font-size: 15px;
  text-align: center;


}




</style>
