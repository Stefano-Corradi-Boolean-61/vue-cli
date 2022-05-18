<template>
  <span>
    <!--            $emit('nomeEventoCustom',parametro)-->
    <button @click="$emit('bottoneCliccato',saluto)" class="btn">BOTTONE saluto</button>
    <button @click="miaFunzionePerEmit" class="btn">BOTTONE con oggetto</button>
  </span>
</template>

<script>
export default {
  name: 'ButtonComponent',
  data(){
    return{
      saluto: 'Ciao mondo'
    }
  },
  methods:{
    miaFunzionePerEmit(){
      const utente = {
        firstname: 'Ugo',
        lastname: 'De Ughi',
      };
      // se uso $emit all'interno di un methods devo precederlo da this
      this.$emit('passaggioUtente',utente);
    }
  }
}
</script>

<style lang="scss" scoped>
  button{
    color: blue;
  }
</style>