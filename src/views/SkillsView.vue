<template>
  <div class="skills">
    <div class="container vh-100 d-flex flex-column justify-content-center align-items-center my-5 text-center">
            
    </div>
  </div>
</template>

<script>
import ProgressBar from '../components/ProgressBar.vue'
export default {
  components: {ProgressBar},
  data(){
    
  }
}
</script>

<style scoped>

.skillIcon{
  position: relative;
  width: 100%;
  height: 350px;
  transition: all 0.6s linear;
  transform-style: preserve-3d;
  background: red;
}

.front,.back{
  position: absolute;
  top:0;
  left:0;
  width:100%;
  height:100%;
  backface-visibility: hidden;

}

#skillsContainer:hover .skillIcon{
  transform: rotateY(180deg);
  
}

.back{
  transform: rotateY(180deg);
}

/* span{
  transition: all 0.3s linear;
  display: block;
}

a:hover{
  transition: all 0.3s linear;
  transform: scale(-1,1);
} */

</style>