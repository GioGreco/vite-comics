<template>
    <footer>
        <div class="footer-top">
            <div class="container">
                <div>
                    <ul> 
                       <li><h4>{{footerLists[0].listTitle}}</h4></li>
                       <li v-for="item in footerLists[0].listItems">{{item}}</li>
                    </ul>
                    <ul>
                        <li><h4>{{footerLists[1].listTitle}}</h4></li>
                        <li v-for="item in footerLists[1].listItems">{{item}}</li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li><h4>{{footerLists[2].listTitle}}</h4></li>
                        <li v-for="item in footerLists[2].listItems">{{item}}</li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li><h4>{{footerLists[3].listTitle}}</h4></li>
                        <li v-for="item in footerLists[3].listItems">{{item}}</li>
                    </ul>
                </div>
                <img src="../assets/img/dc-logo-bg.png" alt="DC logo bg version">
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <div class="shopBtn">shop now</div>
                <div class="socials">
                    <h4>follow us</h4>
                    <img src="../assets/img/footer-facebook.png" alt="Facebook Icon">
                    <img src="../assets/img/footer-twitter.png" alt="Twitter Icon">
                    <img src="../assets/img/footer-youtube.png" alt="YouTube Icon">
                    <img src="../assets/img/footer-pinterest.png" alt="Pinterest Icon">
                    <img src="../assets/img/footer-periscope.png" alt="Periscope Icon">
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import { footerListItems } from '../data/items.js';
    export default {
        name: 'FooterComponent',
        data(){
            return{
                footerLists: footerListItems
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;
@use '../assets/partials/mixins' as *;

footer{
    background-color: $grey-footer-bg;

    .footer-top{
        height: 320px;
        background-image: url('../assets/img/footer-bg.jpg');
        background-size: cover;

        .container{

            @include dflex(row);
            justify-content: flex-start;
            align-items: flex-start;
            height: 100%;
            position: relative;
            overflow: hidden;

            ul{
                list-style: none;
                color: $grey-text-footer;
                font-size: $f-smaller;
                margin-right: 20px;

                h4{
                    font-size: $f-small;
                    color: white;
                    text-transform: uppercase;
                    margin: 12px 0;
                }

                li{
                    padding: 2px 0;

                    &:not(:first-of-type):hover{
                        text-decoration: underline;
                        cursor: pointer;
                    }
                }
            }

            img{
                position: absolute;
                right: 0;
                top: 50%;
                transform: translate(0, -50%);
            }
        }
    }

    .footer-bottom{
        height: 80px;
        .container{
            @include dflex(row);
            height: 100%;

            .shopBtn{
                border: 2px solid $blue-bg;
                padding: 5px 10px;
                text-transform: uppercase;
                color: white;
                font-size: $f-small;
            }

            .socials{
                @include dflex(row);

                width: 40%;

                h4{
                    margin: 0;
                    color: $blue-follow-us;
                    text-transform: uppercase;
                    font-weight: bolder;
                }
            }
        }
    }
}

</style>