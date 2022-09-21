<template>
  <h2>Name: {{ name }}</h2>
  <h3>Age: {{ age }}</h3>
</template>

<script>
export default {
  props: ["name", "age"],
};
</script>

<style>
h2 {
  font-family: sans-serif;
}
h3 {
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
  font-weight: lighter;
}
</style>
