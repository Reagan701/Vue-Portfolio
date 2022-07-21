<template>
<div class="cursor"></div>
  <Navbar />
  <main class="min-vh-100">
    <router-view />
    <!-- v-slot="{Component}">
      <transition name="router" mode="out-in">
        <component :is="Component" ></component>
      </transition>
    </router-view> -->
  </main>
</template>

<script>

let isDay = true;

window.addEventListener("keydown",check);

function check(event){
  console.log(event.keyCode,isDay);
  if(event.keyCode == 32){
    event.preventDefault();
    if(isDay){
      isDay = !isDay;
      document.querySelector(':root').style.setProperty('--background-color',"#071022");
      document.querySelector(':root').style.setProperty('--color',"#2da0ed")
      document.querySelector(':root').style.setProperty('--text-color',"rgb(173,186, 194)");
      // document.querySelector('.sun').classList.remove('goUp');
      // document.querySelector('.sun').classList.add('goDown');
      // document.querySelector('.moon').classList.add('goUp');
      // document.querySelector('.moon').classList.remove('goDown');
      // document.querySelector('.moon').style.display = "block";
      // document.querySelector('.sun').style.display = "none";
    }else{
      isDay = !isDay;
      document.querySelector(':root').style.setProperty('--background-color',"rgb(230, 232, 236)");
      document.querySelector(':root').style.setProperty('--color',"#628aa5")
      document.querySelector(':root').style.setProperty('--text-color',"rgba(var(--bs-body-color-rgb),.75)");
      // document.querySelector('.sun').classList.add('goUp');
      // document.querySelector('.sun').classList.remove('goDown');
      // document.querySelector('.moon').classList.remove('goUp');
      // document.querySelector('.moon').classList.add('goDown');
      // document.querySelector('.moon').style.display = "none";
      // document.querySelector('.sun').style.display = "block";
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
  margin-left: 200px
}
body{
  transition: all 0.3s linear;
  background-color:var(--background-color);
}

:root{
  --background-color:rgb(230, 232, 236);
  --color:#628aa5;
  --text-color:rgba(var(--bs-body-color-rgb),.75);
}

*{
  font-family: 'Poppins',sans-serif;
}

html,body{
  overflow-x: hidden;
}

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
}

/* #paddingLeft{
  margin-left:332px;
  margin-right:332px;
} */

.cursor{
  position:fixed;
  top: 0;
  left: 0;
  width: 10px;
  background-color:rgb(230, 184, 0);
  height: 10px;
  box-shadow: 0px 1rem 4rem #f4c300;
  border-radius: 50%;
}

</style>
