<template>
    <header class="container">
        <div class="logo">
            <a href="#"><img src="../assets/img/dc-logo.png" alt="DC logo"></a>
        </div>
        <navbar>
            <ul>
                <li v-for="(item, index) in navItems" :class="{'active' : item.current}">
                    <a :href="item.link" @mouseover="addActive(index)" @mouseleave="removeActive(index)">{{item.text}}</a>
                </li>
            </ul>
        </navbar>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data(){
            return{
                navItems: [
                    {
                        text: 'characters',
                        link: '#',
                        current: false
                    },
                    {
                        text: 'comics',
                        link: '#',
                        current: false
                    },
                    {
                        text: 'movies',
                        link: '#',
                        current: false
                    },
                    {
                        text: 'tv',
                        link: '#',
                        current: false
                    },
                    {
                        text: 'games',
                        link: '#',
                        current: false
                    },
                    {
                        text: 'collectibles',
                        link: '#',
                        current: false
                    },
                    {
                        text: 'videos',
                        link: '#',
                        current: false
                    },
                    {
                        text: 'fans',
                        link: '#',
                        current: false
                    },
                    {
                        text: 'news',
                        link: '#',
                        current: false
                    },
                    {
                        text: 'shop',
                        link: '#',
                        current: false
                    }
                ]
            }
        },
        methods: {
            addActive(id){
                this.navItems[id].current = true;
            },
            removeActive(id){
                this.navItems[id].current = false;
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;
@use '../assets/partials/mixins' as *;

header{
    @include dflex(row);
    height: 90px;
    
    .logo{
        height: 60px;

        img{
            height: 100%;
        }
    }

    navbar{
        width: 60%;
        height: 100%;

        ul{
            @include dflex(row);
            list-style: none;
            text-transform: uppercase;
            font-size: $f-smallest;
            line-height: 90px;

            .active{
                border-bottom: 5px solid $blue-text-active;
            }

            li{

                a{
                    &:hover{
                        color: $blue-text-active;
                    }

                    text-decoration: none;
                    color: black;
                }
            }
        }
    }
}
</style>