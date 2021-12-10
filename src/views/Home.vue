<template>
  <div class="home">
    <h1>home</h1>
    <p>My name is {{ name }} and age is {{ age }}</p>
    <button @click="handleClick">click me</button>
    <button @click="age++">add 1 to age</button>
    <input type="text" v-model="name" />
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "Home",
  setup() {
    let name = ref("mario");
    let age = ref(18);

    const handleClick = () => {
      name.value = "luigi";
      age.value = 20;
    };

    return {
      name,
      age,
      handleClick,
    };
  },
};
</script>
