<template>

<HomeComponent/>
<TwoWayBinding/>
</template>

<script>

import HomeComponent from './components/HomeComponent.vue';
import TwoWayBinding from './components/TwoWayBinding.vue';


export default {
    name: 'App',
    components: {
        HomeComponent,
        TwoWayBinding
    }
}
</script>

