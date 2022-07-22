<template>
<div class="cursor"></div>
  <Navbar />
  <main class="min-vh-100">
    <router-view 
    v-slot="{Component}">
      <transition name="router" mode="out-in">
        <component :is="Component" ></component>
      </transition>
    </router-view>
  </main>
</template>

<script>

let isDay = true;

window.addEventListener("keydown",check);

function check(event){
  if(event.keyCode == 9){
    event.preventDefault();
    if(isDay){
      isDay = !isDay;
      document.querySelector(':root').style.setProperty('--background-color',"7,16,34");
      document.querySelector(':root').style.setProperty('--color',"#2da0ed")
      document.querySelector(':root').style.setProperty('--text-color',"rgb(173,186, 194)");
      document.querySelector(':root').style.setProperty('--shadow',"0px 1rem 3rem rgba(0,0,0,0.6)");
      document.querySelector(':root').style.setProperty('--brightness',"0.7");
      document.querySelector(':root').style.setProperty('--border',"2px");
      document.querySelector('.cursor').style.display = "block";
      document.querySelector('#sun').style.display = "none";
      document.querySelector('#moon').style.display = "block";
    }else{
      isDay = !isDay;
      document.querySelector('.cursor').style.display = "none";
      document.querySelector(':root').style.setProperty('--background-color',"230, 232, 236");
      document.querySelector(':root').style.setProperty('--color',"#628aa5")
      document.querySelector(':root').style.setProperty('--text-color',"rgba(var(--bs-body-color-rgb),.75)");
      document.querySelector(':root').style.setProperty('--shadow',"0px 1rem 3rem rgba(0,0,0,0.175)");
      document.querySelector(':root').style.setProperty('--brightness',"1");
      document.querySelector(':root').style.setProperty('--border',"3px");
      document.querySelector('#sun').style.display = "block";
      document.querySelector('#moon').style.display = "none";
    }
  }
}

window.addEventListener('mousemove',cursor);

function cursor(event){
  document.querySelector('.cursor').style.top =event.clientY +"px";
  document.querySelector('.cursor').style.left =event.clientX +"px";
}

import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
export default {
  components:{Navbar,Footer}
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

*{
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

main{
  transition: all 0.3s linear;
}

@media screen and (min-width:1600px) {
  main{
    margin-left: 278.725px
  }
}

body{
  transition: all 0.3s linear;
  background-color:rgb(var(--background-color));
}

:root{
  --background-color:230, 232, 236;
  --color:#52748b;
  --text-color:rgba(var(--bs-body-color-rgb),.75);
  --shadow: 0px 1rem 3rem rgba(0,0,0,0.175);
  --brightness: 1
  --border: 3px
}

@media (hover:none) {
  .cursor{
    display: none;
  }  
}


*{
  font-family: 'Poppins',sans-serif;
}

html,body{
  overflow-x: hidden;
}
/* 
.router-enter-from{
  opacity: 0;
  transform: translateY(100px);
}

.router-enter-active{
  transition: all 0.5s ease-out;
}

.router-leave-to{
  opacity: 0;
  transform: translateY(-100px);
}

.router-leave-active{
  transition: all 0.5s ease-in;
} */
.cursor{
  position:fixed;
  top: 0;
  left: 0;
  width: 10px;
  /* background-color:var(--color); */
  height: 10px;
  box-shadow: 0px 0rem 9rem 1.5rem var(--color);
  border-radius: 50%;
}

</style>
