<template>
<h1>Ref in Vue 3</h1>

<input type="text" ref="input" />

<button @click="focusInput">Focus Input</button>

</template>

<script>
export default {
  name: "RefComponent",
  methods: {
    focusInput() {
      this.$refs.input.focus();
      let inputValue = this.$refs.input.value;
      console.log(inputValue);
      this.$refs.input.style.color = "red";
    }
  }
}
</script>

<style scoped>

h1 {
  color: orange;
}
</style>