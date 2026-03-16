<template>
    <h1>CSS Binding</h1>
    <h2 :class="applyStyle">Home Component</h2>
    <button v-on:click="colorfull = !colorfull"> Apply Style</button>
</template>

<script>
export default {
    name: 'ClassBinding',
    data() {
        return {
            colorfull: false
        }
    },
    computed:{
        applyStyle(){
            return {
                green: this.colorfull,
                error: true,
                other: true
            }
        }
    }
}
</script>

<style>

h1{
    color: orange;
}

.green{
    background-color: green;
    width: 200px;
    padding: 10px;

}

.error{
    color: red;
}
.other{
    font-size: 15px;
}
</style>