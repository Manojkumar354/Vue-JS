<template>
<h1>Conditional Component</h1>

<h3 v-if="show">If Condition</h3>

<h3 v-else  >Else Condition</h3>

<button v-on:click="show = !show">Toggle</button>
</template>

<script>
export default {
    data() {
        return {
            show: true
        }
    }
}   
</script>

<style scoped>  </style>