<template>
  <div class="shadow-lg my-5 singleProject">
            <img class="img-fluid" :src="img" :alt=" + 'project'">
              <div class="hoverIcon">
                <div class="ps-3 d-flex align-items-center justify-content-between w-100 h-100">
                  <div class="row">
                    <div class="row">
                      <p class="fs-2" id="title">{{title}} </p>
                    </div>
                    <div class="col-6">
                      <a target="_blank" :href="githubLink">
                      <button class="btn btn-primary"> <i class="bi bi-github"></i> Github</button>
                      </a>
                    </div>
                    <div class="col-6">
                      <a target="_blank" :href="netlifyLink">
                      <button class="btn btn-primary"> <i class="bi bi-globe"></i> Live </button>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
</template>

<script>
export default {
    props:["title","img","githubLink","netlifyLink"]
}
</script>

<style>
.singleProject img {
    height: 25rem;
    max-width: 26rem;
    flex-grow: 1;
    object-fit: cover;
    border: 2px solid black;
}

.singleProject{
  position: relative;
  overflow: hidden;
}

.hoverIcon{
  background-color: var();
  position: absolute;
  top:0;
  bottom:0;
  left:0;
  color:white;
  opacity: 0;
  transition:all 0.5s ease
}

.singleProject img{
  transition:all 1.5s ease
}

.singleProject:hover img{
  transform: scale(1.4);
  /* transform: translate(0px,10px); */
}

.singleProject:hover .hoverIcon{
  opacity: 1;
}
</style>