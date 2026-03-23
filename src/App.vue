<template>
<h1>Simple Form</h1>

<p>{{ form }}</p>

<form>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" v-model="form.email"><br><br>

    <label for="password">Password:</label>
    <input type="password" id="password" name="password" v-model="form.password"><br><br>

    <label for="Country">Country</label>
    <select name="country" id="country" v-model="form.country">
        <option value="">Select a country</option>
        <option value="USA">USA</option>
        <option value="Canada">Canada</option>
        <option value="UK">UK</option>
    </select><br><br>

    <h3>Technology</h3>
    <label for="Java">Java</label>
    <input type="checkbox" id="Java" name="technology" value="Java" v-model="form.technology">
    <label for="Python">Python</label>
    <input type="checkbox" id="Python" name="technology" value="Python" v-model="form.technology">
    <label for="JavaScript">JavaScript</label>
    <input type="checkbox" id="JavaScript" name="technology" value="JavaScript" v-model="form.technology"><br><br>

    <h3>Gender</h3>
    <label for="male">Male</label>
    <input type="radio" id="male" name="gender" value="male" v-model="form.gender">
    <label for="female">Female</label>
    <input type="radio" id="female" name="gender" value="female" v-model="form.gender">
</form>
</template>

<script>
export default {
    name: 'App',
    data() {
        return {
            form: {
                email: '',
                password: '',
                country: '',
                technology: [], 
                gender: ''
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
