<template>
  <main>
    <h1>{{utenteUpper}} {{saluto}}</h1>
    <!-- <ul>
      <li>{{user.name}}</li>
      <li>{{user.lastname}}</li>
      <li>{{user.age}}</li>
    </ul> -->
  </main>
</template>

<script>
export default {
  name: 'MainComponent',
  props:{
    utente:String,
    saluto:String,
  },
  computed:{
    utenteUpper(){
      return this.utente.toUpperCase();
    }
  }
}
</script>

<style>

</style>