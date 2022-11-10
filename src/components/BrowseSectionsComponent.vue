<template>
    <section>
        <div class="container">
            <div v-for="(item, index) in sections" :key="index" class="page">
                <div>
                    <img :src="item.sectionPic" :alt="item.sectionName+' pic'">
                </div>
                <span>{{item.sectionName}}</span>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'BrowseSectionsComponent',
        data(){
            return{
                sections: [
                    {
                        sectionName: 'digital comics',
                        sectionPic: '../src/assets/img/buy-comics-digital-comics.png'
                    },
                    {
                        sectionName: 'dc merchandise',
                        sectionPic: '../src/assets/img/buy-comics-merchandise.png'
                    },
                    {
                        sectionName: 'subscriptions',
                        sectionPic: '../src/assets/img/buy-comics-subscriptions.png'
                    },
                    {
                        sectionName: 'comic shop locator',
                        sectionPic: '../src/assets/img/buy-comics-shop-locator.png'
                    },
                    {
                        sectionName: 'dc power visa',
                        sectionPic: '../src/assets/img/buy-dc-power-visa.svg'
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;
@use '../assets/partials/mixins' as *;


section{
    height: 120px;
    background-color: $blue-bg;
    .container{
        @include dflex(row);
        height: 100%;
        padding: 0 25px;
        .page{

            height: 50px;
            width: calc((100% / 5) - 15px);

            div{
                height: 100%;
                display: inline-block;
                vertical-align: middle;
                margin-right: 10px;
                img{
                    height: 100%;
                }
            }

            span{
                vertical-align: middle;
                text-transform: uppercase;
                font-size: $f-smallest;
                color: white;
                line-height: 50px;
            }

            &:last-of-type div{
                height: 80%;
            }
        }
    }
}

</style>