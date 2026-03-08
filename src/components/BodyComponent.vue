<template>
  <h2>Component body</h2>
  <div>
    <h3>Name: {{ name }}</h3>
    <h3>email: {{ email }}</h3>
    <h3>mobile: {{ mobile == undefined ? 'Not provided' : mobile }}</h3>
    <h3>Address: {{ getAddress('Mukherjee Nagar') }}</h3>
  </div>
</template>

<script>
export default {
    name: 'BodyComponent',
   data() {
        return {
            name: 'Manoj Jaiswal',
            email: 'manoj.jaiswal@example.com',
            mobile: '123-456-7890'
        }
    },
    methods: {
        getAddress: function(location) {
            return `123 Main St, ${location}`;
        }
    }
}
</script>

<style scoped>
h2{
    color: #4242b9;
    text-align: center;
}
h3{
    color: #4242b9;
    text-align: center;
}
</style>