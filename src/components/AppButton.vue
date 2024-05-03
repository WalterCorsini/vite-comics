<script>

</script>

<template>
    <div>
        <span>
            <a @click.prevent href="">
                LOAD MORE
            </a>
        </span>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;
div{
    padding-top: 20px;
    height: 10vh;
    background-color: $black;
    text-align: center;
    a{
        padding: 5px 30px;
        background-color: $blue;
        color: $white;
    }
}
</style>