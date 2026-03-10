<template>
<h1>Pass Data to child component</h1>
<ChildComponent name="Manoj Jaiswal" :user="user" :getData="getData" />
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
    name: 'ParentComponent',
    components: {
        ChildComponent
    },
    data() {
        return {
            user: {
                name: 'Manoj Jaiswal',
                age: 30
            }
        }
    },
    methods: {
        getData() {
            console.warn("Data from parent component")
            alert("Data from parent component")
        }
    }
}
</script>

<style>
h1 {
    color: orange;
}
</style>
