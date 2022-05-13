<template>
  <header>
    <div class="logo">LOGO</div>
    <nav>
      <ul>
        <li>
          <a href="#">link</a>
        </li>
        <li>
          <a href="#">link</a>
        </li>
        <li>
          <a class="active" href="#">link</a>
        </li>
        <li>
          <a href="#">link</a>
        </li>
        <li>
          <a href="#">link</a>
        </li>
        <li>
          <ButtonComponent />
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue";
export default {
    name: "HeaderComponent",
    components: { ButtonComponent }
}
</script>

<style lang="scss" scoped>
// per utilizzarle le mixin e le vars deo importarle nel componente
@import '../assets/style/mixins';
@import '../assets/style/vars';
  header{
    // uso una mixin
    @include center();
    height: 80px;
    // uso una vars
    background-color: $primary-color;
    padding: 15px;
    nav{ 
      ul{
        display: flex;
        list-style: none;
      }
      li a{
          text-decoration: none;
          color: black;
          margin: 10px;
          // & significa l'elemento stesso
          &:hover{
            text-decoration: underline; 
          }
          &.active{
            color: yellow;
          }
      }
      
    }
  }
 
</style>