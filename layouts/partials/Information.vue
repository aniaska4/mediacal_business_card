<template lang="pug">
    section
        div.information
            .image_slider.img
                img.image(src="images/main_picture.jpg" alt="")
            .container.info
                .information_txt
                    h2 Poradnia z pomysłem
                    span Tu znajdziecie Państwo informacje dotyczące naszej pracy 
                    span zapoznacie się z naszą ofertą i pracownikami.
                    span Zapraszamy do umawiania się na wizytę.
                    button
                        a(href="#" class="myButton") Sprawdz ofertę

                .information_places 
                    .contact_informations(v-for="place in places" :class="place.class" )
                        h3 {{ place.name }}
                        .contact
                            span TELEFON |
                            span {{ place.phone }}
                        .border
                        .open_hours
                            .days01
                                span PN | ŚR | PT |
                                span {{ place.hours_01 }}
                            .days02
                                span WT |
                                span {{ place.hours_02 }}
                            .days03
                                span CZ |
                                span {{ place.hours_03 }}
                   
</template>
<script>
export default {
    component: "Information",
    data() {
        return{
            places: [
                {
                class: "blonie_places",
                name: "Błonie",
                phone: "(22) 777 11 22",
                hours_01: "od 7:30 do 16:00",
                hours_02: "od 7:30 do 19:00",
                hours_03: "d 7:30 do 18:00"
                },
                 {
                class: "ozarow_places",
                name: "OŻARÓW MAZOWIECKI",
                phone: "(22) 777 11 22",
                hours_01: "od 7:30 do 16:00",
                hours_02: "od 7:30 do 19:00",
                hours_03: "d 7:30 do 18:00"
                },
                 {
                class: "dziekanow_places",
                name: "DZIEKANÓW LEŚNY",
                phone: "(22) 777 11 22",
                hours_01: "od 7:30 do 16:00",
                hours_02: "od 7:30 do 19:00",
                hours_03: "d 7:30 do 18:00"
                },
                 {
                class: "blizne_places",
                name: "BLIZNE JASIŃSKIEGO",
                phone: "(22) 777 11 22",
                hours_01: "od 7:30 do 16:00",
                hours_02: "od 7:30 do 19:00",
                hours_03: "d 7:30 do 18:00"
                }
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
.information {
    width: 100%;
    .image_slider {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        position: relative;
        flex-direction: column;   
        img {
            width: 100%;
            height: 480px;
        }
    }    
    .info {
        height: 100%;
        position: relative;

        .information_txt {
            height: 78%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: flex-start;
            position: absolute;
            top: -303px;
            h2 {
                margin: 18px 0;
                font-size: 37px;
                letter-spacing: 1.5px;
            }

            span {            
            line-height: 1;
            letter-spacing: 0.4px;
            padding-top: 6px;                
            }
        }

        .information_places {
            .contact_informations {
                height: 247px;
                width: 260px;
                position: absolute;
                top: 15px;
                display: flex;
                flex-direction: column;
                padding: 15px;
                color: $colorWhite;
        
                h3 {
                    text-align: center;
                    font-size: $fontSizeNav;
                    padding: 10px 0 35px 0;
                }
        
                .contact {
                    @include contact_boxes
                }
        
                .open_hours {
                    margin-top: 10px;
                    position: relative;  
                          
                    .days01,
                    .days02,
                    .days03 {
                        @include contact_boxes
                    }
                }        
            }
        
            .blonie_places {
                @include places($colorBlue, -114px, 4px);
        
                .border {
                    @include border(1px, solid, $lightenBlue);
                    margin: 6px 0
                }
                .open_hours{
                    &:before {
                        @include arrow($colorBlue)
                    } 
                }
            }
        
            .ozarow_places {
                @include places($colorGreen, -114px, 297px);
        
                .border {
                    @include border(1px, solid, $lightenGreen);
                    margin: 6px 0
                }

                .open_hours{
                    &:before {
                        @include arrow($colorGreen)
                    }
                }
            }
            .dziekanow_places {
                @include places($colorPink, -114px, 590px);
        
                .border {
                    @include border(1px, solid, $lightenPink);
                    margin: 6px 0
                }
                .open_hours{
                    &:before {
                        @include arrow($colorPink)
                    } 
                }
            }
        
            .blizne_places {
                @include places($colorLightBlue, -114px, 881px);
        
                .border {
                    @include border(1px, solid, $lightenBlue);
                    margin: 6px 0
                }
                .open_hours{
                    &:before {
                        @include arrow($colorLightBlue)
                    } 
                }
            }
        }
    }
}

</style>