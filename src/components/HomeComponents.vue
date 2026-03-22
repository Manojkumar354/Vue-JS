<template>
<h1>Pass Data from home component to child component</h1>

<h2>{{ childUser }}</h2>

    <UserComponents :getUser="getUserName" />
</template>


<script>
import UserComponents from './UserComponents.vue';
export default {
    name: 'HomeComponents',
    data() {
        return {
            childUser: ""
        }
    },
    components: {
        UserComponents
    },
    methods: {
        getUserName(name) {
            this.childUser = name;
        }
    }       
}
</script>

<style>
h2 {
    color: orange;
}
</style>
