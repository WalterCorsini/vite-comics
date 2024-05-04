<script>
import { menuNav } from '../assets/data/products';
export default {
    data() {
        return {
            //  active nav item
            count: 1,
            // array nav bar
            menu: menuNav,
        }
    },
    //  to change active item
    methods: {
        changeActive: function (index) {
            this.menu[this.count].active = false;
            this.count = index;
            this.menu[this.count].active = true;
        }
    }
}
</script>

<template>
    <header>
        
        <!-- logo -->
        <div class="img-header">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <!-- /logo -->

        <!-- nav-list -->
        <ul class="nav">
            <li :class="{ active: curElem.active }" v-for="curElem, i in menu"><a @click.prevent.stop="changeActive(i)"
                    href="">{{ curElem.title }}</a></li>
        </ul>
        <!-- /nav-list -->

    </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;

header {
    @include flex(row, space-between, center);
    height: 15vh;
    line-height: 15vh;
    background-color: $white;

    .img-header {
        @include flex(row, center, center);
        flex-grow: 1;
        img {
            width: 18%;
        }
    }

    .nav {
        @include flex(row, end, center);
        gap: 20px;
        width: 60%;
        margin-right: 100px;

        li {
            font-family: sans-serif;
            font-size: 0.8rem;
            font-weight: 700;
            border-bottom: 5px solid transparent;
            height: 15vh;
        }

        .active {
            border-bottom: 5px solid $blue;
        }
    }
}
</style>