<template lang="pug">
    section
        .footer 
            .container
                .footer_box
                    .footer_box_item(v-for="box in boxes")
                        .footer_box--title 
                            h4 {{ box.title }}
                        .border
                        .footer_box--links
                            span {{ box.link1 }}
                            span {{ box.link2 }}
                            span {{ box.link3 }}
                            span {{ box.link4 }}
                .border_line

    
</template>
<script>
export default {
    component: "Footer",
    data() {
        return{
            boxes: [
                {
                    title: "Nasza poradnia",
                    link1: "Przykładowy link",
                    link2: "Przykładowy link",
                    link3: "Przykładowy link",
                    link4: "Link do podstrony",
                },
                {
                    title: "Oferta",
                    link1: "Przykładowy link",
                    link2: "Przykładowy link",
                    link3: "Przykładowy link",
                    link4: "Link do podstrony",
                },
                {
                    title: "Blog",
                    link1: "Przykładowy link",
                    link2: "Przykładowy link",
                    link3: "Przykładowy link",
                    link4: "Link do podstrony",
                },
                {
                    title: "Informacja",
                    link1: "Przykładowy link",
                    link2: "Przykładowy link",
                    link3: "Przykładowy link",
                    link4: "Link do podstrony",
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
.footer{
    background-color: $colorBlue;
    color: $colorWhite;
    padding-top: 25px;
    padding-bottom: 25px;
}
.footer_box{
    display: flex;
    justify-content: center;
    .footer_box_item{
        width: 70%;
        margin: 10px 10px;
        padding: 10px 5px;
        .footer_box--title{
            margin-bottom: 20px;
            h4{
                font-size: 16px;
            }
        }
        .border {
            width: 80%;
        }
        .footer_box--links {
            margin-top: 20px;
            display: flex;
        flex-direction: column;
            span {
                line-height: 2.2;
                font-size: 12px;
            }
        }
    }
}
.border_line {
    border: 1px solid $lightenBlue;
}
</style>