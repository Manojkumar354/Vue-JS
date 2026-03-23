<template>
<h1>Simple Form</h1>

<p>{{ form }}</p>

<form>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" v-model="form.email"><br><br>

    <label for="password">Password:</label>
    <input type="password" id="password" name="password" v-model="form.password"><br><br>

    <input type="submit" v-on:click="submitForm" value="Submit">
</form>
</template>

<script>
export default {
    name: 'App',
    data() {
        return {
            form: {
                email: '',
                password: ''
            }
        }
    },
    methods: {
        submitForm(event) {
            event.preventDefault();
            console.log(this.form);
        }
    }
}
</script>

<style scoped>
  h1 {
      color: orange;
  }
</style>
