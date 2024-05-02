<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";

export default {
    components:{
        AppHeader,
        AppMain,
    },
    data(){
        return{
            image: "ciao",
        }
    }
}
</script>

<template>
<AppHeader />
<AppMain />
</template>

<style lang="scss">
</style>