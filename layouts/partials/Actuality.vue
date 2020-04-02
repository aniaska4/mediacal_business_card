<template lang="pug">
section
    .news
        .container
            .margin
            .news_title
                h2 Aktualności
            .news_columns
                .column01.space
                    div(v-for="box in column_1" :class="box.class")
                        .img(v-if="box.src")
                            img(:src="box.src")
                        .time
                            i(class="fa fa-clock-o" aria-hidden="true")
                            .data {{ box.data }}
                        .info
                            span {{ box.info }}
                            span {{ box.hour }}
                .column02.space
                    div(v-for="box in column_2" :class="box.class")
                        .img(v-if="box.src")
                            img(:src="box.src")
                        .time
                            i(class="fa fa-clock-o" aria-hidden="true")
                            .data {{ box.data }}
                        .info
                            span {{ box.info }}
                            span {{ box.hour }}
                .column03.space
                    div(v-for="box in column_3" :class="box.class")
                        .img(v-if="box.src")
                            img(:src="box.src")
                        .time
                            i(class="fa fa-clock-o" aria-hidden="true")
                            .data {{ box.data }}
                        .info
                            span {{ box.info }}
                            span {{ box.hour }}
                .column04.space
                    div(v-for="box in column_4" :class="box.class")
                        .img(v-if="box.src")
                            img(:src="box.src")
                        .time
                            i(class="fa fa-clock-o" aria-hidden="true")
                            .data {{ box.data }}
                        .info
                            span {{ box.info }}
                            span {{ box.hour }}
</template>


<script>
export default {
    component: "Actuality",
    data() {
        return {
            column_1: [
                {
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Błoniu ",
                    hour: "czynny do 18:30",
                    class: "small_column small_column_1"                
                },
                {
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Błoniu ",
                    hour: "czynny do 12:30",
                    class: "small_column small_column_2"                
                },
                {
                    src: "images/01.png",
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Błoniu ",
                    hour: "czynny do 15:30",
                    class: "big_column big_column_1"                
                },
            ],
            column_2: [
                {
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Ożarowie ",
                    hour: "czynny do 17:30",
                    class: "small_column small_column_3"                
                },
                {
                    src: "images/01.png",
                    data: "30 LIPCA 2019",
                    info: "Sekretariat poradni w Ożarowie ",
                    hour: "czynny do 14:30",
                    class: "big_column big_column_2"                
                },
                {
                    data: "30 WRZEŚNIA 2019",
                    info: "Sekretariat poradni w Ożarowie ",
                    hour: "czynny do 17:30",
                    class: "small_column small_column_4"                
                },
            ],
            column_3: [
                {
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Dziekanowie ",
                    hour: "czynny do 15:30",
                    class: "small_column small_column_5"                
                },
                {
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Dziekanowie ",
                    hour: "czynny do 16:30",
                    class: "small_column small_column_6"                
                },
                {
                    src: "images/01.png",
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Dziekanowie ",
                    hour: "czynny do 14:30",
                    class: "big_column big_column_3"                
                },
            ],
            column_4: [
                {
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Blizne ",
                    hour: "czynny do 15:30",
                    class: "small_column small_column_7"                
                },
                {
                    src: "images/01.png",
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Blizne ",
                    hour: "czynny do 16:30",
                    class: "big_column big_column_4"                
                },
                {
                    data: "30 CZERWIEC 2019",
                    info: "Sekretariat poradni w Blizne ",
                    hour: "czynny do 12:30",
                    class: "small_column small_column_8"                
                },

            ]
        }
    }    
}
</script>

<style lang="scss" scoped>
@import "styles/scss/variables.scss";
@import "styles/scss/reset.scss";
@import "styles/scss/mixins.scss";
@import "styles/scss/buttons.scss";
@import "styles/scss/rwd.scss";
.news {
    background-color: $colorCreme;

    .news_title {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 34px;

        h2 {
            text-transform: uppercase;
            font-weight: 800;
            font-size: 26px;
            letter-spacing: 2px;
        }
    }

    .small_column,
    .big_column {
        position: relative;
    }

    // Colors in boxes
    @include color-divs-small(1, $colorBlue, 0px);
    @include color-divs-small(2, $colorBlue, 0);
    @include color-divs-small(3, $colorGreen, 0);
    @include color-divs-small(4, $colorGreen, 0);
    @include color-divs-small(5, $colorPink, 0);
    @include color-divs-small(6, $colorPink, 0);
    @include color-divs-small(7, $colorLightBlue, 0);
    @include color-divs-small(8, $colorLightBlue, 0);


    @include color-divs-big(1, $colorBlue, 137px);
    @include color-divs-big(2, $colorGreen, 137px);
    @include color-divs-big(3, $colorPink, 137px);
    @include color-divs-big(4, $colorLightBlue, 137px);

    .news_columns {
        display: flex;
        @media #{$phone, $smallphone} {
          overflow-x: overlay;
        }
        .small_column {
            height: 122px;
            width: 268px;
            border: 1px solid black;
            margin-bottom: 16px;
            display: flex;
            flex-direction: column;
            padding: 14px 21px;

            .time {
                display: flex;
                margin-bottom: 21px;
                margin-top: 7px;

                .fa-clock-o {
                    width: 10%;
                    margin-left: 7px;
                    color: black;
                }

                .data {
                    font-size: 11px;
                    font-weight: 600;
                }
            }

            .info {
                font-size: 13px;
                padding-left: 9px;
                letter-spacing: 0.3px;
            }
        }

        .big_column {
            height: 248px;
            width: 268px;
            margin-bottom: 10px;
            border: 1px solid black;
            margin-bottom: 16px;
            display: flex;
            flex-direction: column;

            .img {
                height: 44%;

                img {
                    height: 100%;
                }
            }

            .time {
                display: flex;
                margin: 41px 0 20px 0;

                .fa-clock-o {
                    width: 10%;
                    margin-left: 25px;
                    color: black;
                }

                .data {
                    font-size: 11px;
                    font-weight: 600;
                }
            }

            .info {
                font-size: 13px;
                padding-left: 9px;
                letter-spacing: 0.3px;
                margin-left: 18px;
                margin-right: 35px;
            }
        }
    }
}
</style>