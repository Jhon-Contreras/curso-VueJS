<template>
  <Navbar/>
  <div class="container">
    <router-view/>
  </div>
</template>


<script>
import {mapActions} from 'vuex'
import Navbar from './components/Navbar'

export default {
    components:{
      Navbar
    },
    methods: {
      ...mapActions(['cargarLocalStorage'])
    },
    // cuando se carge la app, llamamos a la funcion 
    created() {
      this.cargarLocalStorage();
    },
}
</script>