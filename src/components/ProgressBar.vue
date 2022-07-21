<template>
  <div class="mb-5" style="position: relative;">
    <div style="position: relative; margin-bottom:10px;" class=" d-flex justify-content-between align-items-center">
        <h4> {{Title}} </h4>
        <i :class="icon" :style="color"></i>
        <h4> {{width}} </h4>
    </div>
        <div class="progress" id="ProgressBarTop" :style="widthStyle">
            <div class="progress-bar w-100" role="progressbar" :style="backgroundColor" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
            </div>
            <div style="border-radius: 0%" class="progress">
            <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
        </div>
    </div>
</template>

<script>
export default {
    props:["backgroundColor","icon","color","width","widthStyle","Title"]

}
</script>

<style scoped>

#ProgressBarTop{
    border-radius: 0% !important;
}

h4{
    margin:0;
}

i{
    font-size: 2rem;
}

</style>