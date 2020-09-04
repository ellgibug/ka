<template>
    <div class="section border-bottom">
        <div class="container">
            <div class="md-layout">
                <div
                        class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto text-center"
                >
                    <h2 class="title text-center">Занятия в автошколе КречетАвто</h2>
                </div>
            </div>
            <div class="">
                <div class="md-layout">
                    <div class="md-layout-item md-medium-size-100 md-small-size-100">
                        <div class="education">
                            <div class="education__block education-block">
                                <div class="education-block__title">Теоретические занятия</div>
                                <div class="education-block__content">
                                    Теоретические занятия проходят онлайн или в учебном классе рядом с метро
                                    Нагатинская. Занятия проходят по воскресеньям с 9 до 12 часов. На теоретических
                                    занятиях разбираются все вопросы и билеты с экзамена в ГИБДД, а также опытный
                                    преподаватель ответит на все интересующие вас вопросы.
                                </div>
                            </div>
                            <div class="education__block education-block">
                                <div class="education-block__title">Практические занятия</div>
                                <div class="education-block__content">
                                    Автошкола КречетАвто предлагает своим курсантам пройти курс обучения вождению на
                                    автомобилях с МКПП или АКПП. <strong>Занятия начинаются и заканчиваются около метро,
                                    проходят в ЮАО.</strong>
                                    <br>
                                    На выбор предлагаются 2 типа курсов - для тех, кто имеет опыт вождения (20 часов по
                                    60 минут) и для тех, кто впервые за рулем (40 часов по 60 минут).
                                    <br>
                                    Также, по желанию, вы сможете взять дополнительные занятия по цене занятий в курсе
                                    или занятия без заключения основного договора об обучении.
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="md-layout-item md-medium-size-100 md-small-size-100">
                        <img src="../../assets/img/K_A.png" alt="Обучение в автошколе КречетАвто"
                             class="education-image"
                             style="">
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

    .education {
        color: $black-color;
        margin-top: 50px;
        margin-bottom: 30px;

        &__block {
            margin-bottom: 30px;
        }

        &__block:last-child {
            margin-bottom: 0;
        }
    }

    .education-block {
        &__title {
            font-family: $font-family-serif;
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 10px;
        }

        &__content {

        }
    }

    .education-image{
        border-radius: 6px;
        box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
        margin-top: 50px;
        margin-bottom: 30px;
    }

    @media (max-width: 992px) {
        .education-image {
            margin-top: 40px;
        }
    }

    @media (max-width: 768px) {
        .education-image {
            margin-top: 20px;
        }
    }

    @media (max-width: 576px) {
        .education-image {
            margin-top: 10px;
        }
    }
</style>