<template>
  <div class="col-md-2">
                <div class="card py-1 d-flex justify-content-center align-items-center">
                    <i id="skillIcon" style="color:var(--color)" :class="icon"></i>
                    <div class="w-100 card-body">
                        <span class="progressText">{{name}}</span>
                        <progress-bar widthStyle="width:80%" backgroundColor="blue"/>
                    </div>
                </div>
            </div>
</template>

<script>
import ProgressBar from '../components/ProgressBar.vue';
export default {
    props:['name','icon'],
    components:{ProgressBar}
}
</script>

<style scoped>
#skillIcon{
    font-size: 4rem;
}

.progressText{
    height: 26px;
    display: block;
    transition: all 0.3s;
    color:var(--text-color)
}

#progressBar{
    display: none;
}

.card:hover .progressText{
    display: none;
}

.card{
    transition: all 0.4s ease;
    background-color: rgb(var(--background-color));
    border-radius: 0% !important;
    border: none;
    border-bottom: 2px solid var(--color);
    box-shadow: var(--shadow);
}

.card:hover #progressBar{
    display: block;
}

.card:hover{
    transform: scale(1.1);
}
</style>