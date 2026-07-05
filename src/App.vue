<template>
<h1>Simple Form</h1>

<ul>
    <li v-for="item in error" v-bind:key="item">
        {{ item }}
    </li>
</ul>

<form>

    <label for="email">Email:</label>
    <input type="email" id="email" v-model="form.email"><br/><br/>

    <label for="password">Password:</label>
    <input type="password" id="password" v-model="form.password"><br/><br/>

    <label for="country">Country</label>
    <select id="country" v-model="form.country">
        <option value="">Select a country</option>
        <option value="USA">USA</option>
        <option value="Canada">Canada</option>
        <option value="UK">UK</option>
    </select>

    <h3>Technology</h3>
    <label>
        <input type="checkbox" value="Java" v-model="form.technology"> Java
    </label>
    <label>
        <input type="checkbox" value="Python" v-model="form.technology"> Python
    </label>
    <label>
        <input type="checkbox" value="JavaScript" v-model="form.technology"> JavaScript
    </label>

    <h3>Gender</h3>
    <label for="male">Male</label>
    <input type="radio" id="male" value="male" v-model="form.gender">

    <label for="female">Female</label>
    <input type="radio" id="female" value="female" v-model="form.gender">

    <br><br>
    <button type="submit" @click.prevent="submitForm">Submit</button>
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
            },
            error: [],
        }
    },
    methods: {
        submitForm() {
            this.error = [];
            for (const item in this.form) {
                if (this.form[item] === '' || this.form[item].length === 0) {
                    this.error.push(`${item} is required`);
                }
            }

            if (this.error.length === 0) {
                alert('Form submitted successfully!');
            }
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
