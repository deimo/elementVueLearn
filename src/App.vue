<template>
  <div id="app">
    <img alt="Vue logo"
         src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <ElLayout></ElLayout> -->
    <!-- <el-my-container></el-my-container> -->
    <!-- <ELIcon></ELIcon> -->
    <!-- <ElMyButton></ElMyButton> -->
    <!-- <ELRadioDemo></ELRadioDemo> -->
    <!-- <ElCheckBoxDemo></ElCheckBoxDemo> -->
    <!-- <ElInputDemo></ElInputDemo> -->
    <!-- <ElInputDemo2></ElInputDemo2> -->
    <InputNumberDemo></InputNumberDemo>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ElLayout from './components/ElLayout.vue'
import ElMyContainer from './components/ELMyContainer.vue'
import ELIcon from './components/ElIcon.vue'
import ElMyButton from './components/ElMyButton.vue'
import ELRadioDemo from './components/ElRadioDemo.vue'
import ElCheckBoxDemo from './components//ElCheckBoxDemo.vue'
import ElInputDemo from './components/ElInputDemo.vue'
import ElInputDemo2 from './components/ElInputDemo2.vue'
import InputNumberDemo from './components/InputNumberDemo.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    ElLayout,
    ElMyContainer,
    ELIcon,
    ElMyButton,
    ELRadioDemo,
    ElCheckBoxDemo,
    ElInputDemo,
    ElInputDemo2,
    InputNumberDemo,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
