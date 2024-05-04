<template>
    <div class="footer">
        <a @click.prevent href=""><span class="button">SIGN UP NOW</span></a>
        <div class="footer-list">
            <a @click.prevent href=""><span>FOLLOW US</span></a>
            <ul>
                <li><a @click.prevent href=""><img src="../assets/img/footer-facebook.png" alt=""></a></li>
                <li><a @click.prevent href=""><img src="../assets/img/footer-twitter.png" alt=""></a></li>
                <li><a @click.prevent href=""><img src="../assets/img/footer-youtube.png" alt=""></a></li>
                <li><a @click.prevent href=""><img src="../assets/img/footer-pinterest.png" alt=""></a></li>
                <li><a @click.prevent href=""><img src="../assets/img/footer-periscope.png" alt=""></a></li>
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

    .button {
        padding: 5px;
        border: 3px solid $blue;
        transition: 1s;
        color: $white;

        &:hover {
            background-color: $white;
            color: $black;
            border-radius: 20px;
            transition: 1s;
        }
    }

    .footer-list {
        @include flex(row, space-around, center);

        a {
            color: $blue;
        }

        ul {
            @include flex(row, space-around, center);

            li {
                width: 10%;
            }
        }
    }
}
</style>