<template>
    <div class="onemap-page">
        <MapView />
    </div>
</template>

<script>
import MapView from '../components/common/MapView.vue';

export default {
    name: 'OneMap',
    components: {
        MapView
    },
    methods: {

    },
}
</script>

<style>
.onemap-page {
    width: 100%;
    height: 100%;
}
</style>
