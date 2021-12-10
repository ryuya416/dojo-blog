<template>
  <div class="home">
    home
    <p>My name is {{ name }} and age is {{ age }}</p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
export default {
  name: "Home",
  setup() {
    console.log(" setup");

    let name = "mario";
    let age = 30;

    const handleClick = () => {
      console.log("click");
    };

    return {
      name,
      age,
      handleClick,
    };
  },
};
</script>
