<template>
  <div class="about">
    <div id="paddingLeft" class="container h-100 mt-5 d-flex justify-content-center align-items-center flex-column">
        <div class="row mb-5">
            <div class="col-md-1 pe-5">
                <!-- <i id="sun" class="fa-solid fa-sun"></i> -->
            </div>
            <div class="text-center border border-1 pt-3 shadow shadow-lg col-md-11">
                <h1 id="blueColor">Full Stack Development</h1>
                <p id="text" class="fs-5"> I use HTML5, CSS3, Bootstrap and Javascript to create functionial high quality websites</p>
            </div>
        </div>
        <div id="aboutRow" class="row">
                <div class="col-lg-6">
                    <div class="h-100">
                        <img id="ProfessionalImage" class="img-fluid" src="../assets/Reagan1.jpg" alt="SelfImage">
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="ps-lg-5">
                        <div class="row">
                            <div class="col-md-12">
                                <div class="mb-4">
                                    <h2 class="mb-4 underline" id="blueColor"> About Me </h2>
                                    <h3 id="blueColor"> Reagan Carolussen </h3>
                                </div>
                                <div>
                                    <p id="aboutText" class="fs-5"> I am a hard-working, multi-talented individual. I love talking to
                                        people and learning new things. I spend a lot of my free time discovering new
                                        things as well as developing new hobbies. My passion for programming came when I
                                        discovered my love for solving problems and logic-based puzzles. Programming was
                                        the one thing that made me feel like I was doing something I genuinely liked.
                                    </p>
                                </div>
                            </div>
                        </div>
                        <div class="row">
                            <div class="col-md-6">
                                <ul class="d-flex flex-column justify-content-between h-100 list-unstyled">
                                    <li class="mt-3"> <i id="bodyText" class="bi bi-caret-right-fill"></i> <span id="bodyText">Date of Birth</span> <span id="text"> : 03/06/2002</span>  </li>
                                    <li class="mt-3"> <i id="bodyText" class="bi bi-caret-right-fill"></i> <span id="bodyText">Gender</span> <span id="text">: Male </span> </li>
                                    
                                </ul>
                            </div>
                            <div class="ps-0 col-md-6">
                                <ul class="d-flex flex-column justify-content-between h-100 list-unstyled">
                                    <li class="mt-3"> <i id="bodyText" class="bi bi-caret-right-fill"></i> <span id="bodyText" style="word-break:break-all">Email</span> <span id="text">: kingreggie702@gmail.com </span> </li>
                                    <li class="mt-3"> <i id="bodyText" class="bi bi-caret-right-fill"></i> <span id="bodyText">Location</span><span id="text">: South Africa  </span></li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
        </div>
        <div class="row mt-5 w-100">
            <div class="col-md-4">
                <div class="card w-50 py-1 d-flex justify-content-center align-items-center">
                    <i id="skillIcon" style="color:var(--color)" class="fa-brands fa-html5"></i>
                    <div class="card-body">
                        <progress-bar width="100%" style="display:block"/>
                    </div>
                </div>
            </div>
            <div class="col-md-4">
                <div class="card w-50 py-1" style="height:170px">
                    <i id="skillIcon" class="fa-brands fa-html5"></i>
                    <div class="card-body">
                        Text about html
                    </div>
                </div>
            </div>
            <div class="col-md-4">
                <div class="card w-50 py-1" style="height:115px">
                    <i id="skillIcon" class="fa-brands fa-html5"></i>
                    <div class="card-body">
                        Text about html
                    </div>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import ProgressBar from '../components/ProgressBar.vue'
export default {
    components:{ProgressBar}
}
</script>

<style scoped>

#skillIcon{
    font-size: 4rem;
}


    #sun{
        color: rgb(245, 245, 149);
        padding-bottom: 1rem;
        padding-right:15rem;
        font-size: 4rem;
    }

    #text{
        color:var(--text-color)
    }

    #blueColor{
        color:var(--color)
    }

    #aboutText{
        text-align: left;
        /* font-weight: 900; */
        color: var(--text-color) !important;
    }

    #bodyText{
        font-weight: 800;
        color: var(--color)
    }

    ul{
        text-align: left;
    }

    #ProfessionalImage{
        max-width: 450px;
    }

    .underline{
        text-decoration: underline;
        text-decoration-thickness: 2px;
    }

.onHover{
  background-color: rgba(23, 0, 172, 0.26);
  position: absolute;
  top:0;
  bottom:0;
  left:0;
  right:0;
  color:white;
  opacity: 0;
  transition:all 0.3s linear
}

.cont:hover .onhover{
    opacity: 1;
}
</style>