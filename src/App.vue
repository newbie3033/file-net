<template>
  <text-transfer />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import TextTransfer from "./components/TextTransfer.vue";

@Options({
  components: {
    TextTransfer,
  },
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
