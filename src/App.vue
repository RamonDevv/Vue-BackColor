<script>
import {ref} from 'vue'
export default {
  el: '#app',
  data() {
    return  {
      backgroundColor: '#FFFFFF',
      backgroundColorBlue: '#FFFFFF',
      backgroundColorGreen: '#FFFFFF'
    }
  },
 methods: {
  Red: function() {
    alert('Hola Mundo')
  },
  Green:function() {
    console.log("Green")
  },
  Blue:function() {
    console.log ("Blue")
  },
  ChangeBackColorRed() {
    const randomColor = '#' + Math.floor(Math.random()*1677215).toString (16);
    this.backgroundColor = randomColor;
  },
  ChangeBtnBlue() {
    const randomColor = '#' + Math.floor(Math.random()*1677215).toString (16);
    this.backgroundColorBlue = randomColor;
  },
  ChangeBtnGreen() {
    const randomColor = '#' + Math.floor(Math.random()*1677215).toString (16);
    this.backgroundColorGreen = randomColor;
  }
 }
}
</script>

<template>
<main>
  <div class="container-Principal" id="#app">
    <h1>independent Background Changer Vue.js</h1>
  </div>
    <div :style="{ backgroundColor: backgroundColor}" class="Btn1"><button id="btn1" @click="ChangeBackColorRed">Random Background 1</button></div>
    <div :style="{ backgroundColor: backgroundColorBlue}" class="Btn2"><button id="btn2" @click="ChangeBtnBlue">Random Background 2</button></div>
    <div :style="{ backgroundColor: backgroundColorGreen}" class="Btn3"><button id="btn3" @click="ChangeBtnGreen">Random Background 3</button></div>
</main>
</template>

<style scoped>

</style>
