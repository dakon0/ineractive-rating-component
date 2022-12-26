<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <mainComponent v-if="!markSet" @main-component-submitted="toggleToThankComponent"></mainComponent>
  <thanksComponent v-else></thanksComponent>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import mainComponent from './components/mainComponent.vue'
import thanksComponent from './components/thanksComponent.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld
    mainComponent,
    thanksComponent
  },
  data(){
    return {
      markSet: false
    };
  },
  methods: {
    toggleToThankComponent() {
      this.markSet = true;
    }
  }
}
</script>

<style>
  /* #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  } */

  @import url('https://fonts.googleapis.com/css2?family=Overpass:wght@400;700&display=swap'); 

  #app {
    font-family: Overpass, Helvetica, sans-serif;
    /* background-color: hsl(216, 12%, 8%); */

  }



</style>
