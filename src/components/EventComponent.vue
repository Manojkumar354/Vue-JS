<template>
    <div class="event-component">
        <p>{{ title }}</p>
        <p v-on:mousemove="getConsole()">{{ description }}</p>
        <button v-on:click="getCount()">Click Me</button>
        <button v-on:dblclick="getData('Button 2 clicked')">Dubble Click Me</button>
        <p>{{ count }}</p>        
    </div>
</template>

<script>
export default {
    name: 'EventComponent',
    data() {
        return {
            title: 'Event Title',
            description: 'Event description goes here',
            count: 0
        }
    },
    methods: {
        getData(eventId) {
            return alert(eventId);
        },
        getCount() {
            this.count++;
        },
        getConsole() {
            console.log('Mouse moved over description');
        }

    }
}
</script>

<style scoped>
.event-component {
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 4px;
    text-align: center;
}
</style>