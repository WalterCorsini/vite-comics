<script>
import AppFooter from "./components/AppFooter.vue";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";

export default {
    components: {
        AppHeader,
        AppMain,
        AppFooter,
    },
    data() {
        return {
            image: "ciao",
        }
    }
}
</script>

<template>
    <AppHeader />
    <AppMain />
    <AppMainHeader />
    <AppFooter />
</template>

<style lang="scss"></style>