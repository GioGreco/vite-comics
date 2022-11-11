<template>
    <section>
        <div id="current-series" class="container row p-5 position-relative">
            <CoverComponent v-for="(item, index) in covers" :key="index" :obj="item" />
            <div class="banner position-absolute top-0 text-uppercase fs-4 py-1 px-4">
                Current series
            </div>
        </div>
        <div class="p-4">
            <button class="d-block m-auto text-uppercase py-1 px-5 fs-6 fw-bolder">load more</button>
        </div>
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

<style lang="scss">
@use '../assets/partials/variables' as *;

section{

    background-color: $darkgrey;

    #current-series{

        .cover-wrapper{
            color: white;
            font-size: $f-smaller;

            .cover{
                width: 100%;

                img{
                    width: 100%;
                }
            }
        }

        .banner{
            background-color: $blue-bg;
            width: max-content;
            transform: translate(0, -50%);
            color: white;
        }
    }

    button{
        background-color: $blue-bg;
        border: none;
        color: white;
    }
}
</style>