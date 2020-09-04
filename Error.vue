<template>
    <div class="wrapper">
        <div class="section page-header header-filter" :style="headerStyle">
            <div class="container">
                <div class="md-layout">
                    <div
                            class="md-layout-item text-center"
                    >
                        <h1 class="title">Позвоните сюда<br><a href="tel:+74957443642">+7 (495) 744-36-42</a><br>и мы найдем вам страницу :)
                        </h1>

                        <a href="/" class="subtitle">Ваша автошкола КречетАвто</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            header: {
                type: String,
                default: require("@/assets/img/bg_autoschool.png")
            }
        },
        computed: {
            headerStyle() {
                return {
                    backgroundImage: `url(${this.header})`
                };
            }
        }
    };
</script>

<style lang="scss" scoped>
    .title {
        text-shadow: 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 0 1px #f3f7fa, 0 1px 2px rgba(0, 0, 0, .3), 0 3px 9px rgba(0, 0, 0, .1);
        a {
            color: white !important;
            transition: all ease-in-out 0.5s;
        }

        a:hover {
            color: #4caf50 !important;
            transition: all ease-in-out 0.5s;
        }
    }

    .subtitle{
        display: block;
        margin-top: 40px;
        font-weight: 700 !important;
        font-size: 26px;
        color: white !important;
        transition: all ease-in-out 0.5s;
        &:hover{
            color: #4caf50 !important;
            transition: all ease-in-out 0.5s;
        }
    }

    @media (max-width: 992px) {
        .title {
            font-size: 2.9rem
        }
    }

    @media (max-width: 768px) {
        .title {
            font-size: 2.5rem
        }
    }

    @media (max-width: 576px) {
        .title {
            font-size: 2rem
        }
    }
</style>
