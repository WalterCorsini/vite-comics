<script>
import AppHeader from "./components/AppHeader.vue";
import AppTopSubHeader from "./components/AppTopSubHeader.vue"
import AppSubHeader from "./components/AppSubHeader.vue";
import AppBlueRow from "./components/AppBlueRow.vue";
import AppMain from "./components/AppMain.vue";
import AppButton from "./components/AppButton.vue";
import AppFooter from "./components/AppFooter.vue";

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
}
</script>

<template>
    <!-- components Header -->
    <AppHeader />

    <!-- top background subHeader -->
    <AppTopSubHeader />

    <!-- components subHeader -->
    <AppSubHeader />

    <!-- appBlueRow -->
    <AppBlueRow />

    <!-- components main -->
    <AppMain />

    <!-- components footer -->
    <AppFooter />
</template>
