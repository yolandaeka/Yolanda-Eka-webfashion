<template>
  <v-app>
    <NavbarCom />
    <v-content>

      <router-view> </router-view>

    </v-content>


  </v-app>
</template>


<script>

import NavbarCom from '@/components/NavbarCom';


export default {

  name: 'App',
  components: { NavbarCom },
  data(){
    return{

    }
  }
}
</script>

<style>

</style>