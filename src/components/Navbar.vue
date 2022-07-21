<template>

<nav style="z-index:4" class="p-5 navbar text-center fixed-top navbar-expand-lg navbar-light">
        <div class="container p-3 mt-1">
            <button @click="openNav" class="ms-auto navbar-toggler" type="button">
                <span class="bg-white navbar-toggler-icon"></span>
            </button>
        </div>
    </nav>

  <nav id="navbar" class="vh-100 d-flex justify-content-evenly align-items-center flex-column navbar text-center navbar-expand-lg navbar-dark bg-dark">
    <a href="#Landing" class="mx-auto navbar-brand"> Reagan <br>Carolussen </a>
            <div class="navbar-nav d-flex flex-column align-items-center">
                <router-link class="nav-link" to="/"> Home</router-link>
                <router-link class="nav-link" to="/about"> About</router-link>
                <router-link class="nav-link" to="/skills"> Skills</router-link>
                <router-link class="nav-link" to="/resume"> Resumè</router-link>
                <router-link class="nav-link" to="/projects"> Projects</router-link>
                <router-link class="nav-link" to="/testimonials"> Testimonials</router-link>
                <router-link class="nav-link" to="/contact"> Contact</router-link>
            </div>
            <Footer />
    </nav>

</template>

<script>
import Footer from './Footer.vue'

window.addEventListener('resize',changeNav);

function changeNav(){
    if(window.innerWidth > 1600){
        document.getElementById("navbar").style.left = "0"
        document.getElementById("navbar").style.padding = "0px 1rem 0px"
    }else{
        document.getElementById("navbar").style.padding = "0px 0rem 0px"
        document.getElementById("navbar").style.left = "-260px"
    }
}

export default {
    components:{Footer},
    methods:{
        openNav(){
            let nav = document.getElementById("navbar");
            if(nav.style.left == "0" || nav.style.left == "0px"){
                document.getElementById("navbar").style.left = "-260px";
                document.getElementById("navbar").style.padding = "0px 0rem 0px"
            }else{
                document.getElementById("navbar").style.padding = "0px 1rem 0px"
                document.getElementById("navbar").style.left = "0"
            }
        }
    }
}
</script>

<style>

#navbar{
    z-index: 5;
}

</style>