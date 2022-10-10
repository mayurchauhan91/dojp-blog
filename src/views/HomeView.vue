<template>
  <div class="home"></div>
  <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
  <button @click="handleClick">Click me</button>
</template>

<script>
import { ref } from "@vue/reactivity";

export default {
  name: "HomeView",
  setup() {
    const p = ref(null);

    let name = "Mayur";
    let age = 31;
    const handleClick = () => {
      console.log(p, p.value);
      p.value.classList.add("test");
    };

    return { name, age, handleClick, p };
  },
};
</script>
