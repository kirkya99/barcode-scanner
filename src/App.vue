<script>
import { RouterLink, RouterView } from 'vue-router';

export default{
  data(){
    return{
      text: ""
    }
  },
  methods:{
    confirmFunktion(){
      this.text = "Allow access to your camera";
      if(confirm(this.text)==true){
        this.text = "Allowed!";
      }else{
        this.text ="Declined!";
      }
    }
  }
}
</script>

<template>
  <header>
    <h1>Barcode Scanner</h1>
  </header>
  <button @click="confirmFunktion">ConfirmButton</button>
  <p>{{ text }}</p>
</template>

<style>

</style>
