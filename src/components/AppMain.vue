<script>
import { listArray1, listArray2, listArray3, listArray4 } from '../assets/data/products';
export default {
    data() {
        return {
            list1: listArray1,
            list2: listArray2,
            list3: listArray3,
            list4: listArray4,
        }
    },
}
</script>

<template>

    <section>
        <!-- section with list -->
        <div class="main">
            <div>
                <h3>{{ list1.title }}</h3>
                <ul v-for="CurElem in list1.list">
                    <li href=""><a @click.prevent href="">{{ CurElem }}</a></li>
                </ul>

                <h3>{{ list2.title }}</h3>
                <ul v-for="CurElem in list2.list">
                    <li href=""><a @click.prevent href="">{{ CurElem }}</a></li>
                </ul>
            </div>

            <div>
                <h3>{{ list3.title }}</h3>
                <ul>
                    <li v-for="CurElem in list3.list" href=""><a @click.prevent href="">{{ CurElem }}</a></li>
                </ul>
            </div>

            <div>
                <h3>{{ list4.title }}</h3>
                <ul>
                    <li v-for="CurElem in list4.list" href=""><a @click.prevent href="">{{ CurElem }}</a></li>
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

section {
    width: 100%;

    .main {
        @include flex(row, start, start);
        background-image: url(../assets/img/footer-bg.jpg);
        height: 60vh;
        gap: 30px;
        padding-left: 200px;
        padding-top: 10px;
        font-size: 12px;
        font-family: sans-serif;
        position: relative;

        h3 {
            color: $white;
            margin: 20px 0;
        }

        li {
            margin: 7px 0;

            a {
                color: $lightgrey;

                &:hover {
                    background-color: $white;
                    color: $black;
                }
            }
        }

        .main-img {
            position: absolute;
            top: -20%;
            right: 15%;
            width: 35vw;
        }
    }
}
</style>