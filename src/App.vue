<script>
import { defineComponent } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import Test from './components/Test.vue'

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld,
    Test: () => import('./components/Test.vue'),
    Test2: Test,
  },
})
</script>

<template>
  <div id="app">
    <img src="@/assets/logo.svg" alt="Vite logo" />
    <!--<HelloWorld msg="Hello Vue 2 + Vite 3" />-->
    <Test msg="Hello Vue 2 + Vite 3" />
    <Test2 msg="Hello Vue 2 + Vite 3" />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
