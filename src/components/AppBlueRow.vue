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
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;

.main-header{
            @include flex(row,start,center);
            position: relative;
            z-index: 9999;
            padding-left: 200px;
            height: 15vh;
            line-height: 15vh;
            background-color: $blue;
            ul{
                @include flex(row,space-between,center);
                height: 100%;
                width: 80%;
                li{
                    height: 100%;
                    width: calc(100% / 5);
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

</style>