<template>

<HomeComponent/>
<!-- <BodyComponent/> -->
 <EventComponent></EventComponent>

</template>

<script>

import EventComponent from './components/EventComponent.vue';
import HomeComponent from './components/HomeComponent.vue';
// import BodyComponent from './components/BodyComponent.vue';

export default {
    name: 'App',
    components: {
        HomeComponent,
        EventComponent,
        // BodyComponent
    }
}
</script>

