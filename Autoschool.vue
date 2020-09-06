<template>
    <div class="wrapper" id="header">

        <Modal
                v-if="classicModal"
                @close="classicModal = false"
                :placement="placement"/>

        <Header @open="openModal('header')"/>
        <div class="main main-raised">
            <Features id="features"/>
            <Education id="learning"/>
            <Prices id="prices" @open="openModal('prices')"/>
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
    import Modal from "../components/Modal";



    export default {

        components: {
            Modal,
            Header,
            Features,
            Education,
            Prices,
            Contacts
        },

        data() {
            return {
                classicModal: false,
                placement: "header"
            }
        },

        methods: {
            openModal(p) {
                this.placement = p;
                this.classicModal = true;
            }
        },



    };
</script>
<style lang="scss" scoped>
    @import "../assets/scss/material-kit/_variables";

    .main{
        overflow: hidden;
    }
</style>
