<template>
  <div id="app">

    <HeaderComponent />

    <MainComponent :utente="user.name" :saluto="mioSaluto" />

    <FooterComponent />


  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
import MainComponent from "./components/MainComponent.vue";


export default {
    name: "App",
    data(){
      return{
        mioSaluto: 'Ciao ciao',
        mioUtente: 'Giuseppe Verdi',
        user:{
          name:'Ugo',
          lastname:"De Ughi",
          age: 30
        }
      }
    },
    components: { 
      HeaderComponent, 
      FooterComponent, 
      MainComponent 
    }
}
</script>

<style lang="scss">

@import './assets/style/vars';
@import './assets/style/general';
@import './assets/style/utils';

</style>
