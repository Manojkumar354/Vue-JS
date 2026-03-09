<template>
<h1>Welcome to the Home Page</h1>

<input type="text" name="email" placeholder="Email..." v-model="email">  <br/><br/>

<input type="password" name="password" placeholder="password" v-model="password">  <br/><br/>

<button type="button" v-on:click="getData()">Get Values</button>
</template>

<script>
export default {
    name: 'HomeComponent',
    data() {
        return {
            email: '',
            password: ''
        }
    },
    methods: {
        getData() {
            console.log(this.email, this.password);
        }
    }
}
</script>

<style scoped>
h1 {
    color: #42b983;
    text-align: center;
}

</style>
