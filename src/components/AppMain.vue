<script>

</script>

<template>
    <main>
        <div class="text">
            --> content goes here <--
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;
    main{
        @include flex(row,center,center);
        width: 100%;
        height: 12vh;
        background-color: $black;
        color: $white;
        .text{
            width: 70%;
        }
    }
</style>