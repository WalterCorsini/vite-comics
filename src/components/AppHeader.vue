<script>
export default{

}
</script>

<template>
    <header>
        <div class="img-header">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <ul class="nav">
            <li><a href="">CHARACTERS</a></li>
            <li><a href="">COMICS</a></li>
            <li><a href="">MOVIES</a></li>
            <li><a href="">TV</a></li>
            <li><a href="">GAMES</a></li>
            <li><a href="">COLLECTIBLES</a></li>
            <li><a href="">VIDEOS</a></li>
            <li><a href="">FANS</a></li>
            <li><a href="">NEWS</a></li>
            <li><a href="">SHOP</a></li>
        </ul>
    </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;

header{
    @include flex(row,space-between,center);
    padding: 20px;
    height: 15vh;
    background-color: $white;
}

.img-header{
    @include flex(row,center,center);
    flex-grow: 1;
    img{
        width: 18%;
    }
}

.nav{
    @include flex(row,end,center);
    gap: 20px;
    width: 60%;
    margin-right: 100px;
    li{
        padding: 32px 0;
        font-family: sans-serif;
        font-size: 0.8rem;
        font-weight: 700;
        border-bottom: 5px solid transparent;
        &:hover{
            border-bottom: 5px solid $blue;
        }
    }

}
</style>