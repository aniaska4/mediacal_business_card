<template lang="pug">
    section
        .location
            .container
                .location_title
                    h2 Sprawdź jak do nas dojechać
                .location_map
                    iframe(src="https://www.google.com/maps/d/u/0/embed?mid=1xoQ9Ngii0AVcceKlxSrxieSb8yeh6-qU" )    
                .location_title
                    h2 Terminy pracy zespołów orzekających
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
                    name: "Błonie",
                    hours: "Poniedziałki: 7:30 - 16:00",
                    class: "blue"
                },
                {
                    name: "Ożarów Mazowiecki",
                    hours: "Poniedziałki: 9:30 - 18:00",
                    class: "green"
                },
                {
                    name: "Dziakanów Leśny",
                    hours: "Poniedziałki: 10:30 - 17:00",
                    class: "pink"
                },
                {
                    name: "Blizne Jasińskiego",
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
    .blue{
        @include locations_contact($colorBlue)
    }
    .green{
        @include locations_contact($colorGreen)
    }
    .pink{
        @include locations_contact($colorPink)
    }
    .lightBlue{
        @include locations_contact($colorLightBlue)
    }
}

</style>