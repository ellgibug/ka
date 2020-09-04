<template>

    <div class="section">
        <div class="container">
            <div class="md-layout">
                <div
                        class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto text-center"
                >
                    <h2 class="title text-center">Контакты</h2>
                </div>
            </div>
            <div class="">
                <div class="md-layout">
                    <div class="md-layout-item md-medium-size-100 md-small-size-100">
                        <div class="contacts">
                            <div class="contacts__item contacts-item">
                                <i class="fa fa-map" ></i>
                                <span>ЮАО: метро Коломенская, метро Нагатинская<br/>Нагатинская улица, д. 3б</span>
                            </div>
                            <div class="contacts__item contacts-item">
                                <i class="fa fa-calendar"></i>
                                Без выходных, 08:00 - 20:00
                            </div>
                            <div class="contacts__item contacts-item">
                                <i class="fa fa-phone"></i>
                                <a href="tel:+74957443642">+7 (495) 744-36-42</a>
                            </div>
                            <div class="contacts__item contacts-item">
                                <i class="fa fa-envelope"></i>
                                <a href="mailto:krechet.autoshool@gmail.com">krechet.autoshool@gmail.com</a>
                            </div>
                        </div>
                    </div>
                    <div class="md-layout-item md-medium-size-100 md-small-size-100">
                        <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3Abd12110ccd411bb05a152d7c6532d7286dcfd72fb5d7f2d8e489732c6ccc353b&amp;source=constructor" width="100%" height="400" frameborder="0" class="map"></iframe>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped lang="scss">

    @import "../../assets/scss/material-kit/_variables";

    .map {
        width: 100%;
        height: 400px !important;
        margin-top: 50px;
        border-radius: 6px;
        box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
    }

    .contacts {
        margin-top: 50px;
        &__item{
            font-size: 18px;
            color: $black-color;
            padding: 15px 0;
            display: flex;
            align-items: center;
            i{
                margin-right: 10px;
                font-size: 22px !important;
                color: #8c8e90 !important;
                width: 30px;
            }
            a {
                color: #4caf50 !important;
                transition: all ease-in-out 0.5s;
                font-weight: 600;
            }
        }
    }

    @media (max-width: 992px) {
        .map, .contacts {
            margin-top: 40px;
        }
    }

    @media (max-width: 768px) {
        .map, .contacts {
            margin-top: 20px;
        }
    }

    @media (max-width: 576px) {
        .map, .contacts {
            margin-top: 15px;
        }

        .contacts__item{
            font-size: 16px;
            padding: 10px 0;
            i{
                margin-right: 5px;
                font-size: 18px !important;
                width: 25px;
            }
        }
    }
</style>