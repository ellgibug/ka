<template>
    <parallax class="section page-header header-filter">
        <div class="container">
            <div class="md-layout">
                <div
                        class="md-layout-item md-size-70 md-small-size-70 md-xsmall-size-100"
                >
                    <h1 class="title">Открыт набор на категорию В МКПП и АКПП</h1>
                    <div class="subtitle" @click="openModal('header')">
                        Начните обучение с полноценного пробного занятия по вождению перед заключением договора
                    </div>
                    <div class="phones">
                        <div class="phones__item">
                            <a href="tel:+74957443642">+7 (495) 744-36-42</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </parallax>
</template>

<script>
    export default {
        name: "Header",

        methods: {
            openModal: function() {

                this.$emit("open");

                ym(66338023,'reachGoal','header-button');

                return true;

            }
        }

    }
</script>

<style scoped lang="scss">
    .title {
        text-shadow: 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 1px 2px rgba(0, 0, 0, .3), 0 3px 9px rgba(0, 0, 0, .1)
    }

    .header-filter {
        background: url("../../assets/img/bg_autoschool.png") center center;
        background-size: cover;
    }

    .subtitle {
        background: rgb(255, 255, 255);
        color: black;
        font-size: 22px;
        padding: 20px;
        line-height: 32px;
        border-radius: 6px;
        box-shadow: 0 0 0 10px rgba(#bdbdbd, 0.5), 0 0 0 10px rgba(#f9f9f9, 0.5);
        animation: subtitle 2s linear infinite;
        font-weight: 500;
        cursor: pointer;
    }

    @keyframes subtitle {
        0% {
            box-shadow: 0 0 0 10px rgba(#bdbdbd, 0.5), 0 0 0 0 rgba(#f9f9f9, 0.5)
        }
        50% {
            box-shadow: 0 0 0 20px rgba(#bdbdbd, 0), 0 0 0 10px rgba(#f9f9f9, 0.5)
        }
        50.0001% {
            box-shadow: 0 0 0 0 rgba(#bdbdbd, 0.5), 0 0 0 10px rgba(#f9f9f9, 0.5)
        }
        100% {
            box-shadow: 0 0 0 10px rgba(#bdbdbd, 0.5), 0 0 0 20px rgba(#f9f9f9, 0)
        }
    }


    .phones {
        margin-top: 40px;
        font-size: 26px;
        font-weight: 700;

        &__item {
            a {
                color: white !important;
                transition: all ease-in-out 0.5s;
            }

            a:hover {
                color: #4caf50 !important;
                transition: all ease-in-out 0.5s;
            }
        }

        &__item:first-child {
            margin-bottom: 20px;
        }

    }

    @media (max-width: 992px) {
        .title {
            font-size: 2.9rem
        }
        .subtitle {
            font-size: 20px;
            padding: 18px;
            line-height: 30px;
        }
    }

    @media (max-width: 768px) {
        .title {
            font-size: 2.5rem;
            color: black;
        }
        .subtitle {
            font-size: 18px;
            padding: 16px;
            line-height: 28px;
        }
    }

    @media (max-width: 576px) {
        .title {
            font-size: 2rem
        }
        .subtitle {
            font-size: 16px;
            padding: 12px;
            line-height: 26px;
        }
    }
</style>