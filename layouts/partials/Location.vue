<template lang="pug">
    section
        .location
            .container
                .location_title
                    h2 Lorem ipsum dolor sit amet
                .location_map
                    iframe(src="https://www.google.com/maps/d/u/0/embed?mid=1xoQ9Ngii0AVcceKlxSrxieSb8yeh6-qU" )    
                .location_title
                    h2 Lorem ipsum dolor sit amet
                .location_adress
                    .location_adress_medical(v-for="adress in adresses" :class="adress.class")
                        .name
                            h4 {{ adress.name }}
                        .hours
                            h5 {{ adress.hours }}
                                   
                                           
</template>
<script>
export default {
    component: "Location",
    data(){
        return{
            adresses: [
                {
                    name: "Nazwa placówki",
                    hours: "Poniedziałki: 7:30 - 16:00",
                    class: "blue"
                },
                {
                    name: "Nazwa placówki",
                    hours: "Poniedziałki: 9:30 - 18:00",
                    class: "green"
                },
                {
                    name: "Nazwa placówki",
                    hours: "Poniedziałki: 10:30 - 17:00",
                    class: "pink"
                },
                {
                    name: "Nazwa placówki",
                    hours: "Poniedziałki: 8:30 - 16:00",
                    class: "lightBlue"
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
@import "styles/scss/rwd.scss";
.location_title{
    display: flex;
    justify-content: center;
    align-content: center;
    margin: 15px 0;
    padding: 15px 15px;
    h2{
        text-transform: uppercase;
        font-weight: 800;
        font-size: 26px;
        letter-spacing: 2px;
    }
}
.location_map{
    margin-bottom: 20px;
    iframe {
        height: 450px;
        width: 100%;
    }
}
.location_adress{
    display: flex;
    justify-content: center;
    margin-bottom: 30px;
    @media #{$phone, $smallphone} {
        flex-wrap: wrap;
    }
    .location_adress_medical{
        width: 70%;
        border: 1px solid black;
        margin: 10px 10px;
        padding: 10px 5px;
        .name{
            display: flex;
            justify-content: center;
            align-items: center;
            h4 {
            font-size: 18px;
            padding: 5px 5px;
            }
        }
        .hours{
            display: flex;
            justify-content: center;
            align-items: center;
            h5 {
            font-size: 14px;
            padding: 5px 5px;
            }
        } 
    }
    
}
    .blue{
        @include locations_contact($colorBlue)        
    }
    .blue:hover{
            @include locations_contact_hover($colorBlue, $colorWhite)
        }


    .green{
        @include locations_contact($colorGreen)
    }
    .green:hover{
            @include locations_contact_hover($colorGreen, $colorWhite)
        }


    .pink{
        @include locations_contact($colorPink);
    }
    .pink:hover{
            @include locations_contact_hover($colorPink, $colorWhite)
        }


    .lightBlue{
        @include locations_contact($colorLightBlue)
    }
    .lightBlue:hover{
            @include locations_contact_hover($colorLightBlue, $colorWhite)
        }

</style>