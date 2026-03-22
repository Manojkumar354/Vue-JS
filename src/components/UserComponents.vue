<template>

<h2>User Components</h2>
<button v-on:click="getUser(userName)">Send User Name</button>

</template>

<script>
export default {
    name: 'UserComponents',
    data() {
        return {
            userName: 'Manoj'    
        }
    },
    props: {
        getUser: {
            type: Function,
            required: true
        }
    },
}
</script>