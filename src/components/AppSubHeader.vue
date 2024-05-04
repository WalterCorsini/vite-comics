<script>
import { arrayComics } from '../assets/data/products';
import AppButton from "./AppButton.vue";

export default {
    components: {
        AppButton,
    },
    data() {
        return {
            array: arrayComics,
        }
    }
}
</script>

<template>
    <div class="container">
    <div class="card-container">
        <!-- card -->
        <div class="card" v-for="curElem in array">
            <img :src="`${curElem.thumb}`" :class="curElem.type === 'comic-book' ? 'comic-book' : 'graphic-novel'">
            <span>{{ curElem.series }}</span>
        </div>
        <!-- /card -->

        <!-- components button -->

        <AppButton title="LOAD MORE" />
    </div>
</div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;

    .container{
        width: 100%;
        height: min-content;
        background-color: $black;
    }
    .card-container {
        @include flex(row, center, center);
        width: 80%;
        padding-top: 30px;
        margin: 0 auto;
        flex-wrap: wrap;
        gap: 10px;

        .card {
            @include flex(column, space-between, center);
            position: relative;
            z-index: 10;
            color: $white;
            width: calc(100% / 6 - 50px / 6);

            img {
                width: 10vw;
                height: 26vh;
                margin-bottom: 10px;

                &:hover {
                    transform: scale(1.1);
                }
            }

            .comic-book {
                border: 2px solid red;
            }

            .graphic-novel {
                border: 2px solid green;
            }

            span {
                display: inline-block;
                height: 30px;
                font-family: sans-serif;
                font-size: 10px;
            }

            span,
            img {
                align-self: flex-start;
            }
        }

        .bg-black {
            background-color: $black;
        }
    }
</style>