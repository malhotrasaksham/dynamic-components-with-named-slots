<template>
  <div id="app">
    <button @click="currentComponent = 'RedContent'">Load Red</button>
    <button @click="currentComponent = 'GreenContent'">Load Green</button>
    <component :is="currentComponent">
      <h2>Black Heading</h2>
      <p slot="colored">Colored content</p>
    </component>
  </div>
</template>

<script>
import RedContent from "@/components/red-content";
import GreenContent from "@/components/green-content";
export default {
  name: "App",
  components: { RedContent, GreenContent },
  data() {
    return {
      currentComponent: undefined
    };
  },
  beforeCreate() {
    this.currentComponent = "RedContent";
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
