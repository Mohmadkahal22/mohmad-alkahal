<template>
    <!-- Header-->
    <HeaderPage />
    <!-- AllBroducts-->
    <AllBroducts />
    <!-- OtherCompany-->

    <OtherCompany />
    <!-- FooTer -->

    <FooTer />

    <router-view />
</template>

<script>
// @ is an alias to /src
import HeaderPage from "@/components/Header.vue";
import AllBroducts from "@/components/AllBroducts.vue";
import FooTer from "@/components/footer.vue";
import OtherCompany from "@/components/OtherCompany.vue";

export default {
    components: {
        HeaderPage,
        AllBroducts,
        OtherCompany,
        FooTer,
    },
};
</script>
<style></style>
