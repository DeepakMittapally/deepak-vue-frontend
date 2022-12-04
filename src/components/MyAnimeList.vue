<template>

    <div :class="anime.UpcomingMangaAvailability ? 'true': 'false' ">
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
    background-color: #264653;
    color: black;
    padding: 1em;
}

.true{
    background-color: #2a9d8f !important;

}
.false{
    background-color: #e76f51 !important;
}


</style>