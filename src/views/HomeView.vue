<template>
  <div class="home vh-100" >
      <!-- <div class="sun"><i class="fa-solid fa-sun"></i></div> -->
      <!-- <div class="moon"><i class="fa-solid fa-moon"></i></div> -->
    <div style="height:100%" class="d-flex container justify-content-center align-items-center">

      <h1>Hi, I am Reagan <br> An Aspiring Web Developer</h1>


    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '../components/Navbar.vue'

export default {
  name: 'HomeView',
  components: {
    Navbar
  }
}
</script>

<style scoped>

*{
  overflow: hidden;
}

.sun{
  font-size: 9rem;
  color: rgb(204, 204, 67);
  animation: float 3s linear infinite;
  /* animation: goDown 0.8s linear infinite; */
}

.moon{
  display: none;
  font-size: 9rem;
  color: rgb(255, 255, 255);
  transform: translate(0,100vh);
  /* animation: float 3s linear infinite; */
  /* animation: goUp 0.8s linear infinite; */
}

@keyframes float {
  0%{transform: translate(0px);}
  50%{transform: translate(0,30px);}
  100%{transform: translate(0px);}
}

.goUp{
  animation: goUp 1s linear both;
}

.goDown{
  animation: goDown 1s linear both;
}

@keyframes goDown {
  0%{transform: translate(0,0);}
  100%{transform: translate(0,100vh);}
}
@keyframes goUp {
  0%{transform: translate(0,100vh);}
  100%{transform: translate(0,0);}
}

  .home{
    background: linear-gradient(rgba(14, 14, 14, 0.247),rgba(110, 110, 110, 0.144)), url('../assets/fullNightTime.png');
    background-attachment: fixed;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
  }

#topImage{
  position: absolute;
  width: 100%;
  top: 0rem;
  left: 0;
  z-index: 1;
}

h1{
  color: white;
}

#middleImage{
  position: absolute;
  width: 100%;
  top: 4.1rem;
  left: 0%;
  right: 0;
  bottom: 0%;
  z-index: 2;
}

#bottomImage{
  position: absolute;
  width: 100%;
  top: 4.1rem;
  left: 0px;
  right: 0;
  bottom: 0;
  z-index: 3;
}

</style>
