<template>

<nav @load="changeNav" style="z-index:4" class="p-5 navbar text-center fixed-top navbar-light">
        <div class="container-fluid p-3 mt-1">
            <button @click="openNav" class="bg-white me-auto navbar-toggler" type="button">
                <span class="navbar-toggler-icon"></span>
            </button>
        </div>
    </nav>

  <nav id="navbar" class="vh-100 d-flex justify-content-between align-items-center flex-column navbar text-center navbar-expand-lg navbar-dark bg-dark">
      <div class="d-flex justify-content-around flex-column align-items-center">
        <div id="iconsContainer" class="d-flex justify-content-center w-100 align-items-center my-5">
            <!-- <i id="sun" class="fa fa-sun"></i>
            <i id="moon" class="fa fa-moon"></i> -->
            <!-- <button @click="openNav" class="btn-close btn-close-white"></button> -->
            <img src="../assets/Reagan1.jpg" class="ms-1" id="image" alt="ProfessionalImage">
        </div>
        <a href="#Landing" class="mx-auto navbar-brand"> Reagan <br>Carolussen </a>
      </div>
            <div class="navbar-nav d-flex flex-column align-items-center">
                <router-link @click="openNav" id="home" class="nav-link" to="/"> Home</router-link>
                <router-link @click="openNav" id="about" class="nav-link" to="/about"> About</router-link>
                <router-link @click="openNav" id="resume" class="nav-link" to="/resume"> Resumè</router-link>
                <router-link @click="openNav" id="projects" class="nav-link" to="/projects"> Projects</router-link>
                <router-link @click="openNav" id="testimonials" class="nav-link" to="/testimonials"> Testimonials</router-link>
                <router-link @click="openNav" id="contact" class="nav-link" to="/contact"> Contact</router-link>
            </div>
            <Footer />
    </nav>

</template>

<script>
import Footer from './Footer.vue'

// window.addEventListener('resize',changeNav);

function changeNav(){
    if(window.innerWidth > 1600){
        return false
    }else{
        return true
    }
}

export default {
    components:{Footer},
    data(){
        return{
            isOpen:true,
            closeNav:false
        }
    },
    methods:{
        openNav(event){
            if(event.composedPath()[0].id == this.$route.name){
                let nav = document.getElementById("navbar");
                if(this.isOpen){
                    this.isOpen = !this.isOpen
                    nav.style.left = "-278.725px !important";
                }else{
                    this.isOpen = !this.isOpen
                    nav.style.left = "0px !important"
                }
            }else{
                let nav = document.getElementById("navbar");
                if(this.isOpen){
                    this.isOpen = !this.isOpen
                    nav.style.left = "-278.725px !important";
                    document.getElementsByTagName('main')[0].style.marginLeft = "0px";
                }else{
                    this.isOpen = !this.isOpen
                    nav.style.left = "0px !important"
                    document.getElementsByTagName('main')[0].style.marginLeft = "278.725px";
                }
            }
        },
        changeNav(){
            if(window.innerWidth > 1600){
                this.closeNav = false;
                this.isOpen = true;
            }else{
                this.closeNav = true;
                this.isOpen = true;
            }
        }
    }
}
</script>

<style>

.nav-link{
    font-size: 20px !important;
}

#image{
    width:100px;
    border-radius: 50% !important;
}

@media screen and (max-width:1600px) {
    /* #navbar{
        left: -278.725px !important
    } */
}

#navbar{
    z-index: 5;
    left:0px
}

#moon{
    display: none;
}

#moon,#sun{
    font-size:2rem;
    color:var(--color)
}


#iconsContainer{
    gap:8rem
}

</style>