<script>

</script>

<template>
    <section>
        <div class="header">
            --> content goes here <--
        </div>
        <div class="main-header">
                <ul>
                    <li>
                        <a href="">
                        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                        DIGITAL COMICS
                        </a>
                    </li>
                    <li>
                        <a href="">
                        <img src="../assets/img/buy-comics-merchandise.png" alt="">
                        DC MERCHANDISE
                        </a>
                    </li>
                    <li>
                        <a href="">
                        <img src="../assets/img/buy-comics-subscriptions.png" alt="">
                        SUBSCRIPTION
                        </a>
                    </li>
                    <li class="img-locator">
                        <a href="">
                        <img src="../assets/img/buy-comics-shop-locator.png" alt="">
                        COMIC SHOP LOCATOR
                        </a>
                    </li>
                    <li>
                        <a href="">
                        <img src="../assets/img/buy-dc-power-visa.svg" alt="">
                        DC POWER VISA
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
                width: 80%;
                @include flex(row,center,center);
            }

            li a{
                @include flex(row,center,center);
                color: $white;
                font-size: 0.5rem;
            }
            img{
                width: 20%;
                margin-right: 10px;
            }
            .img-locator{
                width: 15%;    
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