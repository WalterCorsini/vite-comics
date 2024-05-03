<script>
export default {
    props: {
        elemImage: String,
        elemSeries: String,
    },
}
</script>

<template>
    <!-- card -->
        <div class="card">
            <img :src="elemImage">
            <span>{{ elemSeries }}</span>
        </div>
        <!-- /card -->
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;


    .card {
        @include flex(column,space-between,center);
        position: relative;
        z-index: 9999;
        color: $white;
        width: calc(100% / 6 - 50px / 6);
        img {
            width: 11vw;
            height: 24vh;
            margin-bottom: 10px;
        };
        span{
            display: inline-block;
            height: 30px;
            font-family: sans-serif;
            font-size: 10px;
        }
        span,img{
            align-self: flex-start;
        }
    }
</style>