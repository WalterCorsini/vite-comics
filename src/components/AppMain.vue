<script>
export default{
    data(){
        return{
            image:[
                {
                    image: "buy-comics-digital-comics.png",
                    title: "DIGITAL COMISCS",
                },
                {
                    image: "buy-comics-merchandise.png",
                    title: "DC MERCHANDISE",
                },
                {
                    image: "buy-comics-subscriptions.png",
                    title: "SUBSCRIPTION",
                },
                {
                    image: "buy-comics-shop-locator.png",
                    title: "COMIC SHOP LOCATOR",
                },
                {
                    image: "buy-dc-power-visa.svg",
                    title: "DC POWER VISA",
                },
                   ] 
        }
    },
    methods:{
        dynamicImage: function(curImg){
            return new URL(`../assets/img/${curImg}`, import.meta.url).href;
        }
    },
}
</script>

<template>
    <section>
        <div class="header">
            --> content goes here <--
        </div>
        <div class="main-header">
                <ul>
                    <li v-for="img,i in image">
                        <a href="">
                        <img :class="i === 0 || i === 3 ? 'big-img' : ''" :src="dynamicImage(img.image)" alt="" />
                        {{ img.title }}
                    </a>
                    </li>
                </ul>
            
        </div>
        <div class="main">
            <div>
                <h3>DC COMICS</h3>
                <ul>
                    <li><a href="">Characters</a></li>
                    <li><a href="">Comics</a></li>
                    <li><a href="">Movies</a></li>
                    <li><a href="">tv</a></li>
                    <li><a href="">Games</a></li>
                    <li><a href="">video</a></li>
                    <li><a href="">News</a></li>
                </ul>
                <h3>SHOP</h3>
                <ul>
                    <li><a href="">Shop Dc</a></li>
                    <li><a href="">Shop Dc Collectibles</a></li>
                </ul>
            </div>
            <div>
                <h3>DC</h3>
                <li><a href="">Terms Of Use</a></li>
                <li><a href="">Privacy policy(New)</a></li>
                <li><a href="">Ad Choices</a></li>
                <li><a href="">Advertising</a></li>
                <li><a href="">Jobs</a></li>
                <li><a href="">Subscriptions</a></li>
                <li><a href="">Talent WorkShops</a></li>
                <li><a href="">CPSC Certificates</a></li>
                <li><a href="">Ratings</a></li>
                <li><a href="">Shop Help</a></li>
                <li><a href="">contact Us</a></li>
            </div>

            <div>
                <h3>SITES</h3>
                <ul>
                    <li><a href="">DC</a></li>
                    <li><a href="">MAD Magazines</a></li>
                    <li><a href="">DC Kids</a></li>
                    <li><a href="">Dc Universe</a></li>
                    <li><a href="">Dc Power Visa</a></li>
                </ul>
            </div>
            <div class="main-img">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;
    
section{
    width: 100%;
    .header{
            @include flex(row,start,center);
            position: relative;
            background-color: $black;
            height: 10vh;
            padding-left: 200px;
        }
        color: $white;
        .main-header{
            @include flex(row,start,center);
            position: relative;
            z-index: 9999;
            padding-left: 200px;
            height: 15vh;
            background-color: $blue;
            ul{
                height: 100%;
                width: 80%;
                @include flex(row,space-between,center);
                li{
                    height: 100%;
                    width: calc(100% / 5);
                    padding-top: 22px;
                    img{
                        width: 20%;
                    }
                    &:hover{
                        border-bottom: 5px solid black;
                    }
                }
                .big-img{
                    width: 15%;
                }
                .four-img{
                    width: 10%;
                }
                

            }
            a{
                @include flex(row,center,center);
                gap: 10px;
                color: $white;
                font-size: 0.5rem;
            }

        }
        
        .main{
            @include flex(row,start,start);
            font-family: sans-serif;
            font-size: 8px;
            padding-left: 200px;
            padding-top: 10px;
            gap: 30px;
            background-image: url(../assets/img/footer-bg.jpg);
            height: 50vh;
            h3{
                margin: 20px 0;
            }
            li{
                margin: 7px 0; 
            }
            a{
                color: $lightgrey;
                &:hover{
                    text-decoration: underline;
                    background-color: $white;
                    color: $black;
                }
            }
            .main-img{
                position: absolute;
                top: 30%;
                right: 15%;
                width: 30%;
            }
            
        }
    }
</style>