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
            <li>CHARACTERS</li>
            <li>COMICS</li>
            <li>MOVIES</li>
            <li>TV</li>
            <li>GAMES</li>
            <li>COLLECTIBLES</li>
            <li>VIDEOS</li>
            <li>FANS</li>
            <li>NEWS</li>
            <li>SHOP</li>
        </ul>
    </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;

header{
    @include flex(row,space-between,center);
    padding: 20px;
    height: 100px;
    background-color: $white;
}

.img-header{
    @include flex(row,center,center);
    flex-grow: 1;
    img{
        width: 10%;
    }
}

.nav{
    @include flex(row,end,center);
    gap: 20px;
    width: 60%;
    margin-right: 100px;
    li{
        padding: 40px 0;
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