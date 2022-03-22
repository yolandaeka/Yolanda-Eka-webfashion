<template>
  <v-card color="basil">
    <v-card-title class="text-center justify-center py-6">
      <h1 class="text-change">
        DOROTHEA
      </h1>
    </v-card-title>

    <v-tabs class="tab-change"
      v-model="tab"
      background-color="transparent"
      color="#DCC5A0"
      grow
    >
      <v-tab
        v-for="item in items"
        :key="item"
      >
        {{ item }}
      </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item
        v-for="item in items"
        :key="item"
      >
        <v-card
          color="basil"
          flat
        >
         
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>

</template>


<script>

export default {
    data () {
      return {
        tab: null,
        items: [
          'HOME', 'READY-TO-WEAR', 'HIJAB', 'FRAGARANCE', 'ABOUT', 'CONTACT'
        ]
      }
    },
  }




</script>


<style>

@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@700&family=Montserrat:wght@500&display=swap');

 .text-change{
  font-family: 'Merriweather',serif;
  font-size: 35px;
  letter-spacing: 4px;

}

.tab-change{
  font-family:'Montserrat', sans-serif;
}


</style>