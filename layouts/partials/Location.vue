<template lang="pug">
    section
        .location
            .container
                .location_title
                    h2 Sprawdź jak do nas dojechać
                .location_map
                    iframe(src="https://www.google.com/maps/d/u/0/embed?mid=1xoQ9Ngii0AVcceKlxSrxieSb8yeh6-qU" )                    
                                           
</template>
<script>
export default {
    component: "Location",
    data(){
        return{

        }
    }
}
</script>
<style lang="scss" scoped>
.location_title{
    display: flex;
    justify-content: center;
    align-content: center;
    margin: 15px 0;
}
.location_map{
    margin-bottom: 20px;
    iframe {
        height: 450px;
        width: 100%;
    }
}

</style>