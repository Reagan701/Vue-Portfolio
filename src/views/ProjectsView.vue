<template>
  <div class="projects">
    <div class="container h-100 my-5 d-flex justify-content-center align-items-center flex-column">
      <div class="row">
        <h2>Here are my works</h2>
      </div>
      <div class="row">
        <div v-for="project in projects" :key="project.id" class="col-md-4">
          <projectItem :title="project.title" :img="project.img" :githubLink="project.githubLink" :netlifyLink="project.netlifyLink"/>
        </div>

      </div>
      </div>
    </div>
</template>

<script>

import projectItem from '../components/projectItem.vue'

export default {
  components:{ projectItem },
  data(){
    return{
      projects:[
        {
          id:1,
          img:"https://i.postimg.cc/mZ7kjDQ1/Rainbow.png",
          title:"A Rainbow created using HTML and CSS",
          githubLink:'https://github.com/Reagan701/Rainbow',
          netlifyLink: 'https://reagan-rainbow.netlify.app/'
        },
        {
          id:2,
          img:'https://i.postimg.cc/nr1HJXkd/Holiday-Destination.png',
          title:"A small website I created using HTML and CSS that shows my favourite holiday desitination",
          githubLink:'https://github.com/Reagan701/HolidayDestination',
          netlifyLink: 'https://reaganholidaydestination.netlify.app/'
        },
        {
          id:3,
          img:'https://i.postimg.cc/52FrfRWQ/Calculator.png',
          title:"A functional Calculator created using Javascript, using HTML and CSS",
          githubLink:'https://github.com/Reagan701/Calculator',
          netlifyLink: 'https://reagancalculator.netlify.app'
        },
        {
          id:4,
          img:'https://i.postimg.cc/tCRZ0KPD/Mock-Portfolio.png',
          title:"A Mock Portfolio made with HTML and CSS",
          githubLink:'https://github.com/Reagan701/DesignPortfolio',
          netlifyLink: 'https://carolussen-portfolio.netlify.app/'
        },{
          id:5,
          img:'https://i.postimg.cc/G2kvY1rW/Pokedex.png',
          title:"A Pokédex made with Javascript and API's",
          githubLink: 'https://github.com/Reagan701/Pokedex_Api',
          netlifyLink: 'reagan-pokedex.netlify.app'
        },{
          id:6,
          img:'https://i.postimg.cc/8CBdyvxs/Property-App.png',
          title:'A mock property listing project, with functional CRUD systems',
          githubLink: 'https://github.com/Reagan701/ListingProject',
          netlifyLink:'https://reagan-listing-project.netlify.app'
        },{
          id:7,
          img:'https://i.postimg.cc/vTwP1MR6/To-doApp.png',
          title:'An app created using Javascript that allows you to track your activities To-Do App',
          githubLink: 'https://github.com/Reagan701/toDoApp',
          netlifyLink:'https://reagan-to-do-app.netlify.app'
        }
      ]
    }
  }
}
</script>

<style scoped>



</style>