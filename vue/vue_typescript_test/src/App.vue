<template>
  <HelloWorld />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld from "./components/Welcome.vue";

export default defineComponent({
  name: "App",
  components: {
    HelloWorld,
  },
});

const add = (a : number, b: number) => a + b;
console.log(add(1, 3))
const object = {
  method1: function() {
    return this;
  }
}
console.log(object.method1)
</script>

