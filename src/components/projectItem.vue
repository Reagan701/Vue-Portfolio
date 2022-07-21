<template>
  <div class="my-5 singleProject">
            <img class="img-fluid" :src="img" :alt=" + 'project'">
              <div class="hoverIcon">
                <div class="ps-3 d-flex align-items-center justify-content-between w-100 h-100">
                  <div class="row">
                    <div class="row">
                      <p class="fs-2" id="title">{{title}} </p>
                    </div>
                    <div class="col-6 m-0">
                      <a target="_blank" :href="githubLink">
                      <button class="hoverButton"> <i class="bi bi-github"></i> Github</button>
                      </a>
                    </div>
                    <div class="col-6 m-0">
                      <a target="_blank" :href="netlifyLink">
                      <button class="hoverButton"> <i class="bi bi-globe"></i> Live </button>
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

<style scoped>
.singleProject img {
    height: 25rem;
    flex-grow: 1;
    object-fit: cover;
    filter: brightness(var(--brightness));
}

#title{
  color:var(--color);
}

.hoverButton{
    border-color: var(--color);
    color: var(--color);
    font-weight: 900;
    background-color: transparent;
    border: 0.188rem solid var(--color);
    transition: all 0.2s ease-in-out;
    font-size: 24px;
    padding-left:10px;
    padding-right:10px;
}

.hoverButton:hover {
    background-color: var(--color);
    color: white;
}

.singleProject{
  position: relative;
  overflow: hidden;
  box-shadow: var(--shadow);
}

.hoverIcon{
  background-color: rgba(var(--background-color),0.85);
  position: absolute;
  top:0;
  bottom:0;
  left:0;
  color:white;
  opacity: 0;
  transition:all 0.5s ease
}

.singleProject img{
  transition:transform 1.5s ease, filter 0.7s ease;
}

.singleProject:hover img{
  transform: scale(1.4);
  /* transform: translate(0px,10px); */
}

.singleProject:hover .hoverIcon{
  opacity: 1;
}
</style>