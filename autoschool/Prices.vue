<template>
    <div class="section border-bottom">
        <div class="container">
            <div class="md-layout">
                <div
                        class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto text-center"
                >
                    <h2 class="title text-center">Услуги и цены</h2>
                    <h5 class="description">
                        Цены являются фиксированными и не меняются на протяжении обучения.
                    </h5>
                </div>
            </div>
            <div class="">

                <div class="prices">
                    <div class="prices__block prices-block">
                        <div class="prices-block__title">Теоретический курс</div>
                        <div class="prices-block__content prices-block-content">
                            <div class="prices-block-content__item prices-block-row">
                                <div class="prices-block-row__title">Единоразовая оплата</div>
                                <div class="prices-block-row__price">17 000 Р</div>
                            </div>
                        </div>
                    </div>

                    <div class="prices__block prices-block">
                        <div class="prices-block__title">Практические занятия МКПП</div>
                        <div class="prices-block__content prices-block-content">
                            <div class="prices-block-content__item prices-block-row">
                                <div class="prices-block-row__title">1 час (60 минут) для учеников, заключивших договор
                                    (основное занятие)
                                </div>
                                <div class="prices-block-row__price">800 Р</div>
                            </div>
                            <div class="prices-block-content__item prices-block-row">
                                <div class="prices-block-row__title">1 час (60 минут) для учеников, заключивших договор
                                    (дополнительное занятие)
                                </div>
                                <div class="prices-block-row__price">800 Р</div>
                            </div>
                            <div class="prices-block-content__item prices-block-row">
                                <div class="prices-block-row__title">1 час (60 минут) для учеников, не заключивших договор
                                </div>
                                <div class="prices-block-row__price">1 000 Р</div>
                            </div>
                        </div>
                    </div>

                    <div class="prices__block prices-block">
                        <div class="prices-block__title">Практические занятия АКПП</div>
                        <div class="prices-block__content prices-block-content">
                            <div class="prices-block-content__item prices-block-row">
                                <div class="prices-block-row__title">1 час (60 минут) для учеников, заключивших договор
                                    (основное занятие)
                                </div>
                                <div class="prices-block-row__price">1 000 Р</div>
                            </div>
                            <div class="prices-block-content__item prices-block-row">
                                <div class="prices-block-row__title">1 час (60 минут) для учеников, заключивших договор
                                    (дополнительное занятие)
                                </div>
                                <div class="prices-block-row__price">1 000 Р</div>
                            </div>
                            <div class="prices-block-content__item prices-block-row">
                                <div class="prices-block-row__title">1 час (60 минут) для учеников, не заключивших договор
                                </div>
                                <div class="prices-block-row__price">1 200 Р</div>
                            </div>
                        </div>
                    </div>

                    <div class="prices__description">*Оплата практических занятий происходит по факту проведения занятия.
                        Вам не нужно оплачивать весь курс сразу.
                    </div>
                </div>

                <div class="md-layout">
                    <div
                            class="md-layout-item md-large-size-25 md-medium-size-50 md-small-size-100"
                            v-for="(course,index) in courses"
                            :key="index"
                    >
                        <div :class="[index === 1 && 'recommended', 'course']">
                            <div class="course__title">
                                {{ course.title }}
                            </div>
                            <div class="course__content course-content">
                                <div class="course-content__item course-content-item">
                                    <div class="course-content-item__title">
                                        <md-icon>check_circle_outline</md-icon>
                                        Индивидуальное расписание практических занятий</div>
                                </div>
                                <div class="course-content__item course-content-item">
                                    <div class="course-content-item__title">
                                        <md-icon>check_circle_outline</md-icon>
                                        Топливный сбор и ГСМ</div>
                                </div>
                                <div class="course-content__item course-content-item">
                                    <div class="course-content-item__title"><md-icon>check_circle_outline</md-icon>Проведение внутреннего экзамена</div>
                                </div>
                                <div class="course-content__item course-content-item">
                                    <div class="course-content-item__title"><md-icon>check_circle_outline</md-icon>Поддержка на протяжении
                                        обучения</div>
                                </div>
                                <div class="course-content__item course-content-item">
                                    <div class="course-content-item__title"><md-icon>check_circle_outline</md-icon>Свидетельство об окончании автошколы</div>
                                </div>
                                <div class="course-content__item course-content-item">
                                    <div class="course-content-item__title"><md-icon>check_circle_outline</md-icon>Теоретические занятия</div>
                                    <div class="course-content-item__price">17 000 Р</div>
                                </div>
                                <div class="course-content__item course-content-item">
                                    <div class="course-content-item__title"><md-icon>check_circle_outline</md-icon>Практические занятия {{course.hours}} ч</div>
                                    <div class="course-content-item__price">{{course.price}} Р</div>
                                </div>
                            </div>
                            <div class="course__price">
                                {{course.total_price}} Р
                            </div>
                        </div>
                    </div>
                </div>


                <div class="md-layout md-alignment-center">
                    <md-button class="md-success md-lg" @click="openModal">Записаться</md-button>
                </div>
            </div>

        </div>
    </div>
</template>

<script>
    export default {
        name: "Header",
        data(){
            return{
                courses: [
                    {
                        title: 'МКПП базовый',
                        hours: '20',
                        price: '16 000',
                        total_price: '33 000'
                    },
                    {
                        title: 'МКПП полный',
                        hours: '40',
                        price: '32 000',
                        total_price: '49 000'
                    },
                    {
                        title: 'АКПП базовый',
                        hours: '20',
                        price: '20 000',
                        total_price: '37 000'
                    },
                    {
                        title: 'АКПП полный',
                        hours: '30',
                        price: '30 000',
                        total_price: '47 000'
                    },
                ]
            }
        },
        methods: {
            openModal: function() {
                this.$emit("open");

                ym(66338023,'reachGoal','prices-button');

                return true;
            }
        }

    }
</script>

<style scoped lang="scss">
    @import "../../assets/scss/material-kit/_variables";

    .description {
        color: $black-color;
        font-size: 18px;
    }

    .course {
        margin-top: 70px;
        margin-bottom: 30px;
        background: #fafafa;
        box-sizing: border-box;
        border-radius: 6px;
        box-shadow: 0px 5px 10px 2px rgba(34, 67, 80, 0.2);
        transition: all ease-in-out 0.5s;
        &.recommended{
            /*box-shadow: 0px 5px 10px 2px rgba(76, 175, 80, 0.8);*/
            border: 2px solid #4caf50;
        }

        &:hover {
            box-shadow: none;
            transition: all ease-in-out 0.5s;
            background: white;
        }

        &__title {
            font-size: 20px;
            padding: 24px 6px;
            font-weight: 600;
            text-align: center;
            font-family: $font-family-serif;
        }

        &__content {

        }

        &__price {
            font-family: $font-family-serif;
            font-size: 26px;
            font-weight: 600;
            padding: 24px 6px;
            text-align: center;

        }
    }

    @media (max-width: 992px) {
        .course {
            margin-top: 40px;
            margin-bottom: 30px;
        }
    }

    @media (max-width: 768px) {
        .course {
            margin-top: 20px;
            margin-bottom: 20px;
        }
    }

    @media (max-width: 576px) {
        .course {
            margin-top: 15px;
            margin-bottom: 15px;
        }
    }

    .course-content-item {
        display: flex;
        justify-content: space-between;
        font-size: 14px;
        padding: 10px 6px;

        &__price {
            font-family: $font-family-serif;
            min-width: 60px;
            text-align: right;
        }

        &__title {
            line-height: 16px;
            display: flex;
            align-items: center;

            i{
                margin-right: 3px;
                color: #4caf50 !important;
                font-size: 22px !important;
            }
        }
    }

    .prices {
        margin-top: 50px;

        &__block {
            margin-bottom: 30px;
        }
    }

    .prices-block {
        &__title {
            font-family: $font-family-serif;
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 10px;
        }

        &__content {

        }
    }

    .prices-block-content {
        &__item {
            border-bottom: 1px solid #e3e3e3;
            padding-bottom: 10px;
            margin-bottom: 10px;
        }

        /*&__item:hover {*/
        /*    background: #f3f3f3;*/
        /*}*/

        &__item:last-child {
            border-bottom: none;
        }
    }

    .prices-block-row {
        display: flex;
        justify-content: space-between;
        align-items: center;

        &__price {
            font-family: $font-family-serif;
            min-width: 60px;
            text-align: right;
        }
    }

    @media (max-width: 576px) {
        .prices-block-row{
            font-size: 14px;
            line-height: 18px;
        }
    }
</style>