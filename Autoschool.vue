<template>
    <div class="wrapper" id="header">

        <Header/>
        <div class="main main-raised">
            <Features id="features"/>
            <Education id="learning"/>
            <Prices id="prices"/>
            <Contacts id="contacts"/>
        </div>
    </div>
</template>

<script>

    import Header from "./autoschool/Header";
    import Features from "./autoschool/Features";
    import Education from "./autoschool/Education";
    import Prices from "./autoschool/Prices";
    import Contacts from "./autoschool/Contacts";

    export default {

        components: {
            Header,
            Features,
            Education,
            Prices,
            Contacts
        }
    };
</script>
<style lang="scss" scoped>
    @import "../assets/scss/material-kit/_variables";

    .main{
        overflow: hidden;
    }
</style>
