<template>

<HomeComponent/>
<BodyComponent/>

</template>

<script>

import HomeComponent from './components/HomeComponent.vue';
import BodyComponent from './components/BodyComponent.vue';

export default {
    name: 'App',
    components: {
        HomeComponent,
        BodyComponent
    }
}
</script>

