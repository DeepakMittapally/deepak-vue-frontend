<template>
 <div class="container">
    <MyHeader titleName="Animes" 
      details ="info about animes" />
    <MyAnimeDetails :animes="animes"/>
    <MyAbout About=" extra details about website"/>

 </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyAnimeDetails from './components/MyAnimeDetails.vue'
import MyAbout from './components/MyAbout.vue'


export default{
name:'App',
components: {
  MyHeader,
  MyAnimeDetails,
  MyAbout

},

data(){
    return {
      animes: [],
      isHidden: false
    }
  },
  methods: {
    // promises

      async fetchAnime(){
         const res= await fetch("https://deepak-node-backend.onrender.com/api")
         const data= await res.json()
          console.log(data, data.animes)
         return data.animes
      }

  },

  async created(){
    this.animes = await this.fetchAnime()
  }
}
 
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
.container {
  max-width: 600px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
  background-color: #EFE7BC;
}

div{
  margin-bottom: 0.5em;
}
</style>
