<template>
    <header class="container">
        <div class="logo">
            <a href="#"><img src="../assets/img/dc-logo.png" alt="DC logo"></a>
        </div>
        <nav>
            <ul>
                <li v-for="(item, index) in navItems" :key="index" :class="{'active' : item.current, 'watched' : beingWatched(index)}">
                    <a :href="item.link" @mouseover="addActive(index)" @mouseleave="removeActive(index)">{{item.text}}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data(){
            return{
                activePage: 2,
                navItems: [
                    {
                        id: 1,
                        text: 'characters',
                        link: '#',
                        current: false
                    },
                    {
                        id: 2,
                        text: 'comics',
                        link: '#',
                        current: false
                    },
                    {
                        id: 3,
                        text: 'movies',
                        link: '#',
                        current: false
                    },
                    {
                        id: 4,
                        text: 'tv',
                        link: '#',
                        current: false
                    },
                    {
                        id: 5,
                        text: 'games',
                        link: '#',
                        current: false
                    },
                    {
                        id: 6,
                        text: 'collectibles',
                        link: '#',
                        current: false
                    },
                    {
                        id: 7,
                        text: 'videos',
                        link: '#',
                        current: false
                    },
                    {
                        id: 8,
                        text: 'fans',
                        link: '#',
                        current: false
                    },
                    {
                        id: 9,
                        text: 'news',
                        link: '#',
                        current: false
                    },
                    {
                        id: 10,
                        text: 'shop',
                        link: '#',
                        current: false
                    }
                ]
            }
        },
        methods: {
            beingWatched(i){
                if(this.activePage == this.navItems[i].id){
                    return true;
                }
            },
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

    nav{
        width: 60%;
        height: 100%;

        ul{
            @include dflex(row);
            list-style: none;
            text-transform: uppercase;
            font-size: $f-smallest;
            line-height: 90px;

            li{
                &.watched{
                    box-shadow: inset 0 -10px 0 -5px $blue-text-active;
                }
                &.active{
                    box-shadow: inset 0 0px 0 0px $blue-text-active;
                    transition: box-shadow .2s ease-in-out;
                }

                &.active:hover{
                    box-shadow: inset 0 -10px 0 -5px $blue-text-active;
                }

                a{
                    display: inline-block;

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