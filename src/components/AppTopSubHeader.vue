<script>
import AppButton from "./AppButton.vue";
export default {
    components: {
        AppButton,
    },
}
</script>

<template>
    <div class="container">
        <div class="button">
            <AppButton title="CURRENT SERIES" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    background-image: url("../assets/img/jumbotron1.jpg");
    position: relative;
    background-size: cover;
    background-repeat: no-repeat;
    width: 100%;
    height: 50vh;

    .button {
        position: absolute;
        z-index: 9999;
        bottom: -10%;
        left: 10%;
    }
}
</style>
