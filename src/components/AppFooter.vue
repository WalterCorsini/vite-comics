<script>

</script>

<template>
    <div class="footer">
        <span class="button"><a href="">SIGN UP NOW</a></span>
        <div class="footer-list">
            <span><a href="">FOLLOW US</a></span>
            <ul>
                <li><a href=""><img src="../assets/img/footer-facebook.png" alt=""></a></li>
                <li><a href=""><img src="../assets/img/footer-twitter.png" alt=""></a></li>
                <li><a href=""><img src="../assets/img/footer-youtube.png" alt=""></a></li>
                <li><a href=""><img src="../assets/img/footer-pinterest.png" alt=""></a></li>
                <li><a href=""><img src="../assets/img/footer-periscope.png" alt=""></a></li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;

.footer {
    @include flex(row, space-around, center);
    position: relative;
    gap: 100px;
    z-index: 9999;
    height: 10vh;
    width: 100%;
    font-family: sans-serif;
    font-weight: 700;
    background-color: $darkgrey;

    .button a {
        padding: 5px;
        border: 3px solid $blue;
        color: $white;

        &:hover {
            background-color: $white;
            color: $black;
        }
    }

    .footer-list a {
        color: $blue;
    }

    .footer-list,
    ul {
        @include flex(row, space-around, center);
    }

    li {
        width: 10%;
    }
}
</style>