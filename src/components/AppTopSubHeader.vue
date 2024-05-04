<script>
import AppButton from "./AppButton.vue";
export default{
    components:{
        AppButton,
    },
}
</script>

<template>
<div class="container">
    <img src="../assets/img/jumbotron.jpg" alt="">
    <div class="button">
        <AppButton title="CURRENT SERIES"/>
    </div>
</div>
</template>

<style>
    .container {
        position: relative;
        background-size: cover;
        width: 100%;
        height: 40vh;
        margin-bottom: 20px;
        .button{
            position: absolute;
            z-index: 9999;
            top: 35%;
            left: 10%;
        }
    }
</style>
