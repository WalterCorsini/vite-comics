<script>
    export default{
        props:{
            title:String,
        }
    }
</script>

<template>
    <div>
        <span>
            <a @click.prevent href="">
                {{ title }}
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
    text-align: center;
    a{
        padding: 5px 30px;
        background-color: $blue;
        color: $white;
    }
}
</style>