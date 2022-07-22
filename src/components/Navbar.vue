<template>

<nav @load="changeNav" style="z-index:4" class="p-0 navbar text-center fixed-top navbar-light">
        <div class="container-fluid p-0 p-1 mt-1">
            <button id="navButton" @click="openNav" class="me-auto navbar-toggler" type="button">
                <span class="navbar-toggler-icon"></span>
            </button>
        </div>
    </nav>

  <nav id="navbar" style="left:0px" class="vh-100 d-flex justify-content-between align-items-center flex-column text-center navbar-expand-lg navbar-dark bg-dark">
      <div class="d-flex justify-content-around flex-column align-items-center">
        <div id="iconsContainer" class="d-flex justify-content-center w-100 align-items-center my-5">
            <div class="d-flex align-items-center flex-column justify-content-center">
                <span class="text-white mb-4">Click Me! <br>(or press tab)</span>
                <i @click="check" id="sun" class="fa fa-sun"></i>
                <i @click="check" id="moon" class="fa fa-moon"></i>
            </div>
            <button @click="openNav" class="btn-close btn-close-white"></button>
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

export default {
    components:{Footer},
    data(){
        return{
            isOpen:true,
            closeNav:false,
            isLight:true
        }
    },
    methods:{
        openNav(event){
            if(event.composedPath()[0].id == this.$route.name){
                return;
            }else{
                let nav = document.getElementById("navbar");
                if(this.isOpen){
                    this.isOpen = !this.isOpen
                    nav.style = "left:-278.725px !important";
                    if(window.innerWidth <501){
                        nav.style.width = "auto";
                    }else{
                        document.getElementsByTagName('main')[0].style.marginLeft = "0px";
                    }
                }else{
                    this.isOpen = !this.isOpen
                    nav.style = "left: 0px !important"
                    if(window.innerWidth <501){
                        nav.style.width = "100%";
                    }else{
                        document.getElementsByTagName('main')[0].style.marginLeft = "278.725px";
                    }
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
        },
        check(event){
            if(event.keyCode == 9 || event.button == 0){
                if(event.keyCode == 9){
                    event.preventDefault();
                }
            if(this.isLight){
                this.isLight = !this.isLight;
                document.querySelector(':root').style.setProperty('--background-color',"7,16,34");
                document.querySelector(':root').style.setProperty('--color',"#2da0ed")
                document.querySelector(':root').style.setProperty('--text-color',"rgb(173,186, 194)");
                document.querySelector(':root').style.setProperty('--shadow',"0px 1rem 3rem rgba(0,0,0,0.6)");
                document.querySelector(':root').style.setProperty('--brightness',"0.7");
                document.querySelector(':root').style.setProperty('--border',"2px");
                document.querySelector('#sun').style.display = "none";
                document.querySelector('#moon').style.display = "block";
            }else{
                this.isLight = !this.isLight;
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
#navButton{
    padding-top:10px;
    padding-bottom:10px;
    border-radius: 5px !important;
    background-color:var(--color) ;
    box-shadow: var(--shadow);
}

#navbar{
    z-index: 5;
        position: fixed;
        top:0;
        left:0;
        transition: all 0.3s linear;
    }

#moon{
    display: none;
}

#moon,#sun{
    font-size:2rem;
    color:var(--color);
    padding:10px;
    /* border:2px solid var(--color); */
    border-radius:50%;
    cursor: pointer;
    box-shadow: 0 0 0 0 green;
    animation: effect 3s infinite
}

@keyframes effect {
    0%{box-shadow: 0 0 4px 4px;}
    50%{box-shadow: 0 0 17px 9px;}
    100%{box-shadow: 0 0 4px 4px;}
}


#iconsContainer{
    gap:6rem
}

</style>