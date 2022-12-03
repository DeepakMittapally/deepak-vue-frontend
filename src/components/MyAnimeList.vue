<template>

    <div :class="anime.UpcomingMangaAvailability ? 'Blue': 'red' ">
        <h2>{{anime.title}}</h2>
        <div class = "A">
            <p>
                <ul>
                    <li><b>CONTENTS</b></li>
                    &nbsp;&nbsp;<u>Year of Release:</u> {{anime.yearOfRelease}}<br>
                    &nbsp;&nbsp;<u>genre:</u> {{anime.genre}}<br>
                    &nbsp;&nbsp;<u>IMDB Rating:</u> {{anime.IMDBRating}}<br>
                </ul>
            </p>
        </div>
    </div>
</template>

<script>

export default{
    name: 'MyAnimeList',
    props:{
        anime: Array
    }  
}
</script>

<style scoped>



h4{
    margin: 2px;
}

div{
    background-color: #E7F2F8;
    color: black;
    padding: 1em;
}

.red{
    background-color: #74BDCB !important;

}
.Blue{
    background-color: #FFA384 !important;
}


</style>