<template>
    <section id="current-series">
        <CoverComponent/>
    </section>
</template>

<script>
import CoverComponent from './CoverComponent.vue';
import { comics } from '../data/items.js'

    export default {
        name: 'CurrentSeriesComponent',
        components: {
            CoverComponent
        },
        data(){
            return{
                covers: comics
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>