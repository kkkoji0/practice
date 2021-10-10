<template>
  <div class="hello">
    <h1>{{ fullName }} {{ this.user.age }}</h1>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";

export interface User {
  firstName: string;
  lastName: string;
  age: number;
}

export default defineComponent({
  name: 'HelloWorld',
  props: {
    user: {
      type: Object as PropType<User>,
      required: true,
    }
  },
  computed: {
    fullName(): string {
      return this.user.firstName + ' ' + this.user.lastName
    }
  }
})
</script>