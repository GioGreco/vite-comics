<template>
    <div class="cover-wrapper col-2">
        <div class="cover">
            <img :src="obj.thumb" :alt="obj.series">
        </div>
        <div class="text-uppercase py-3 px-2">
            {{obj.series}}
        </div>
    </div>
</template>

<script>
    export default {
        name: 'CoverComponent',
        props: ['obj']
    }
</script>