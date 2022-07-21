<template>
  <div id="resumeContainer" class="resume">
    <div id="paddingLeft" class="container my-5 min-vh-100">
      <div class="d-flex justify-content-center h-100 align-items-center">
        <div class="row">
          <div class="col-md-6">
            <div class="headingContainer">
              <h2 id="title"> Education </h2>
            </div>
            <ResumeCard v-for="experience in educationExperiences" :key="experience.id" :name="experience.name" :message="experience.message" :date="experience.date" :img="experience.img"  />
            </div>
            <div class="col-md-6">
              <div>
                <h2 id="title"> Work Experience </h2>
              </div>
              <ResumeCard v-for="experience in workExperiences" :key="experience.id" :name="experience.name" :message="experience.message" :date="experience.date" :img="experience.img"  />
              </div>
            </div>
          </div>
      </div>
        </div>
</template>

<script>
import ResumeCard from '../components/ResumeCard.vue'

export default {
  components:{ResumeCard},
  mounted(){
    window.scrollTo(0,0);
  },
  data(){
    return{
      educationExperiences:[
        {
          id:1,
          name: "Life Choices Academy",
          message: "Currently studying Web-Development and Coding at Life Choices Academy",
          date:"2022 - Present",
          link:"https://www.lifechoices.co.za/academy",
          img:"https://i.postimg.cc/QMn92ytB/Life-Choices-Logo.png"
        },
        {
          id:2,
          name: "Academic Institute of Excellence",
          message: "Studied Video Game Design and Development at AIE where I graduated with the bronze award",
          date:"2020",
          link:"https://www.aie.ac/",
          img:"https://i.postimg.cc/MpHKKSdK/AIE-logo-1280x720-removebg-preview.png"
        },
        {
          id:3,
          name: "Mondale High School",
          message: "Attended Mondale High School from 2015-2019 where I marticulated with a Bachelors doing Pure Maths, Life Sciences, Geography and Physics.",
          date:"2015-2019",
          link:"http://www.mondalehs.co.za/",
          img:"https://i.postimg.cc/0QT6QK7P/Mondale-High.jpg"
        },
        
      ],
      workExperiences:[
        {
          id:1,
          name: "Virtual World",
          message: "Job Shadowed in Grade 10 at Virtual World, where I learned how management works in professional spaces",
          date:"2017",
          link:"http://www.virtualworld.capetown/",
          img:"https://static.wixstatic.com/media/ab8381_7fc19164cc184b67a0a6218c34daa214~mv2.jpg/v1/fill/w_716,h_200,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ab8381_7fc19164cc184b67a0a6218c34daa214~mv2.jpg"
        },
        {
          id:2,
          name: "CPOA Yvonne Parfitt Place",
          message: "Currently studying Web-Development and Coding at Life Choices Academy",
          date:"2017",
          img:"https://i.postimg.cc/sfbJJjGb/CPOA-removebg-preview.png",
          link:"https://cpoa.co.za/estate_property/yvonne-parfitt-place-retirement-village/"
        },
      ]
    }
  }
}
</script>

<style scoped>

#title{
  color:var(--color)
}

#resumeContainer{
  margin-bottom:200px
}
#resumeCard{
  min-height: 31.25rem;
}

</style>