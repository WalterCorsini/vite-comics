<script>
export default {
    props: {
        elemImage: String,
        elemSeries: String,
        elemType: String,
    },
}
</script>

<template>
    <!-- card -->
        <div class="card">
            <img :src="elemImage"
            :class="elemType === 'comic book' ? 'comic-book' : 'graphic-novel'">
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
    z-index: 10;
    color: $white;
    width: calc(100% / 6 - 50px / 6);
    img {
        width: 10vw;
        height: 26vh;
        margin-bottom: 10px;
        &:hover{
            transform:scale(1.1);
        }
    }
    .comic-book{
        border:1px solid red;
    }
    .graphic-novel{
        border:1px solid green;
    }
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