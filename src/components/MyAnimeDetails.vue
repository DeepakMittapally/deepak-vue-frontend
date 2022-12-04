<template>
    <div class="animedetails">
        <div v-for="anime in animes" :key="anime.id" >     
               <MyAnimeList :anime="anime"/>
        </div>
    </div>

</template>

<script>
import MyAnimeList from "./MyAnimeList.vue"
export default {
    name: 'MyAnimeDetails',
    components: {
        MyAnimeList
    },
    props:{
        animes: Array

    }
}


</script>


<style>
.animedetails{

    background-color:#f4a261;
    border: 5px solid black;
    padding: 1em;
    color: gray;
}

</style>