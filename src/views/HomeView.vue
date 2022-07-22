<template>
  <div class="home vh-100" >
    <div style="height:100%" class="d-flex flex-column container justify-content-start align-items-center">

      <h1 id="shadow" style="color:var(--color); margin-top:1.5rem;padding:2rem; border-radius:10px; opacity:.7;">Hi, I am Reagan <br> An Aspiring Web Developer</h1>


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

#shadow{
  box-shadow: var(--shadow);
}

.sun{
  font-size: 9rem;
  color: rgb(204, 204, 67);
  animation: float 3s linear infinite;
}

.moon{
  display: none;
  font-size: 9rem;
  color: rgb(255, 255, 255);
  transform: translate(0,100vh);
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
    background: url('../assets/fullNightTime.png');
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
