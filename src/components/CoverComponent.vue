<template>
    <div class="cover-wrapper col-2">
        <div class="cover position-relative">
            <img :src="obj.thumb" :alt="obj.series">
            <div class='comic-info position-absolute w-100 h-100 top-0'>
                <div class="position-absolute bottom-0 end-0">
                    <span class="price d-block">{{obj.price}}</span>
                    <span class="type d-block text-uppercase">{{obj.type}}</span>
                </div>
            </div>
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