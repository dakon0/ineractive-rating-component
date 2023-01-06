<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <mainComponent class="main" v-if="!markSet"
                 @main-component-submitted="toggleToThankComponent"
                 @mark-one-clicked="setMarkToOne"
                 @mark-two-clicked="setMarkToTwo"
                 @mark-three-clicked="setMarkToThree"
                 @mark-four-clicked="setMarkToFour"
                 @mark-five-clicked="setMarkToFive"></mainComponent>
  <thanksComponent v-else :markNumber="markNum"></thanksComponent>
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
  data() {
    return {
      markSet: false,
      markNum: 0
    };
  },
  methods: {
    toggleToThankComponent() {
      this.markSet = true;
    },
    setMarkToOne(){
      this.markNum = 1;
    },
    setMarkToTwo(){
      this.markNum = 2;
    },
    setMarkToThree(){
      this.markNum = 3;
    },
    setMarkToFour(){
      this.markNum = 4;
    },
    setMarkToFive(){
      this.markNum = 5;
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

  height: 90vh;
  display: flex;
  justify-content: center;
  align-items: center;

}
</style>
