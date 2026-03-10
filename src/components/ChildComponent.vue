<template>
<h2>Name: {{ user.name }}</h2>
<h2>Age: {{ user.age }}</h2>

<button @click="getData()">Call Function</button>
</template>

<script>

export default {
    name: 'ChildComponent',
    props: {
        name: String,
        user: Object,
        getData: Function
    }
}
</script>
