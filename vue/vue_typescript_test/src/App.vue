<template>
  <HelloWorld :user="user"/>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld, {User} from "./components/HelloWorld.vue";



export default defineComponent({
  name: "App",
data(){
  return {
    person:{
      firstName: 'John',
      lastName: 'doe',
      age: 30,
    } as User
  }
},
computed:{
  user(): User {
    return this.person;
  }
},
components: {
  HelloWorld,
}
});

</script>

