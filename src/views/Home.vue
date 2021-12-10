<template>
  <div class="home">
    <h1>home</h1>
    <p ref="p">My name is {{ name }} and age is {{ age }}</p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "Home",
  setup() {
    const p = ref(null);
    console.log(p, p.value);

    let name = "mario";
    let age = 30;

    const handleClick = () => {
      console.log(p, p.value);
      p.value.classList.add("test");
      p.value.textContent = "test";
    };

    return {
      name,
      age,
      handleClick,
      p,
    };
  },
};
</script>
