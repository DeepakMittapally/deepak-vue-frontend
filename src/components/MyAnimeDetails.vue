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

    background-color: bisque;
    border: 5px solid #4C5270;
    padding: 1em;
    color: gray;
}

</style>