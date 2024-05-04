<script>
export default{
    data(){
        return{
        }
    },  

}
</script>

<template>

    <section>
        <!-- blue row with icon -->
        <!-- /blue row with icon -->

        <!-- section with list -->
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
        <!-- /section with list -->

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

        
        .main{
            @include flex(row,start,start);
            position: relative;
            font-family: sans-serif;
            font-size: 12px;
            padding-left: 200px;
            padding-top: 10px;
            gap: 30px;
            background-image: url(../assets/img/footer-bg.jpg);
            height: 60vh;
            h3{
                margin: 20px 0;
            }
            li{
                margin: 7px 0; 
            }
            a{
                color: $lightgrey;
                &:hover{
                    background-color: $white;
                    color: $black;
                }
            }
            .main-img{
                position: absolute;
                top: -20%;
                right: 15%;
                width: 35vw;
            }
            
        }
    }
</style>