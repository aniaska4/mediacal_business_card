<template lang="pug">
    header
        .nav.container
            .nav_title
                .nav_img
                    img(src="images/logo.png" alt="logo")
                .nav_description
                    h1 Zespół Poradni Rehabilitacyjnej Powiatu Warszawskiego Zachodniego
                    .nav_places
                        span(v-for="place in places") {{ place }}
            .main_nav
                ul
                    li 
                        i.fas.fa-home
                    li.scroll(v-for="nav in navBar") {{ nav }}             
</template>
<script>
export default {
    component: "Nav",
    data(){
        return{
            places: ["Błonie", "Ożarów Mazowiecki", "Dziekanów Leśny", "Blizne Jasińskiego"],
            navBar: ["Nasza poradnia", "aktualności", "oferta", "do pobrania", "blog", "kontakt" ]
        }
    }
}
</script>
<style lang="scss" scoped>
@import "styles/scss/variables.scss";
@import "styles/scss/reset.scss";
.nav_title {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    margin-top: 20px;

    .nav_img {
        width: 184px;

        img {
            width: 71%;
        }
    }

    .nav_description {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;

        h1 {
            font-size: $fontSizeTitle;
            border-bottom: 1px solid $colorSilver;
            font-weight: 400;
            width: 100%;
            padding-bottom: 16px;
            margin-top: 19px;
            letter-spacing: -0.4px;
        }

        .nav_places {
            display: flex;
            flex-direction: row;
            justify-content: flex-start;
            padding-top: 8px;
            span {
                padding: 5px 32px 5px 20px;
                font-weight: 800;
                color: $colorBlue;
                font-size: 13px;
                text-transform: uppercase;
                border-right: 1px solid $colorSilver;
            }
            span:nth-child(1){
                padding: 5px 22px 5px 0;
            }
        }
    }
}

.main_nav {
    background-color: $colorBlue;
    margin-top: 15px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    width: 100%;
    ul {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        list-style-type: none;
        text-transform: uppercase;
        color: $colorWhite;
        font-weight: 500;
        font-size: 12px;
        width: 76%;
        margin-bottom: 6px;
        li {
            padding: 25px 21px;
            letter-spacing: 1px;
        }
    }
}

</style>style
