<script>
import AppHeader from "./components/AppHeader.vue";
import AppTopSubHeader from "./components/AppTopSubHeader.vue"
import AppSubHeader from "./components/AppSubHeader.vue";
import AppBlueRow from "./components/AppBlueRow.vue";
import AppMain from "./components/AppMain.vue";
import AppButton from "./components/AppButton.vue";
import AppFooter from "./components/AppFooter.vue";
import { arrayComics } from "./assets/data/products.js";

export default {
    components: {
        AppHeader,
        AppSubHeader,
        AppTopSubHeader,
        AppBlueRow,
        AppButton,
        AppMain,
        AppFooter,
    },
    data() {
        return {
            // hero array
            array: arrayComics,
        }
    }
}
</script>

<template>
    <!-- components Header -->
    <AppHeader />

    <!-- top background subHeader -->
    <div class="top-subheader">
        <AppTopSubHeader />
    </div>
    

     <div class="container">
        <!-- components subHeader -->
          <div class="card-container"> 
            <AppSubHeader
                class="card"
                v-for="curElem in array" :elemImage="curElem.thumb"
                :elemSeries="curElem.series" :elemType="curElem.type" />
                
                <!-- components button -->
                <div class="bg-black">
                <AppButton title="LOAD MORE"/>
                </div>
            </div>
        </div> 

            <!-- appBlueRow -->
            <AppBlueRow />

            <!-- components main -->
            <AppMain />

    <!-- components footer -->
    <AppFooter />
</template>

<style lang="scss" scoped>
@use "./style/partials/variable" as *;
@use "./style/partials/mixin" as *;

.top-subheader{
    height: 50vh;
}

.container {
    height:min-content ;
    background-color: $black;
    margin: 0;

    .card-container {
        @include flex(row, center, center);
        width: 80%;
        padding-top: 30px;
        margin: 0 auto;
        flex-wrap: wrap;
        gap: 10px;
    }
}
.bg-black{
    background-color: $black;
}
</style>