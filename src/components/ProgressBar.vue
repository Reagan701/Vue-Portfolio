<template>
  <div id="progressBar" style="height:26px;position: relative;">
    <div style="position: relative; margin-bottom:10px;" class=" d-flex justify-content-between align-items-center">
    </div>
        <div class="progress" id="ProgressBarTop" :style="widthStyle">
            <div class="progress-bar w-100" role="progressbar" style="background-color: var(--color)" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100">{{width}}</div>
            </div>
            <div style="border-radius: 0%;background-color:var(--text-color)" class="progress">
            <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
        </div>
    </div>
</template>

<script>
export default {
    props:["widthStyle","width"]
}
</script>

<style scoped>

#ProgressBarTop{
    border-radius: 0% !important;
    position: absolute;
    top: 0;
    left: 0;
}

h4{
    margin:0;
}

i{
    font-size: 2rem;
}

</style>