<template>
  <div class="col-md-2">
                <div class="card py-4 d-flex flex-column justify-content-between align-items-center">
                    <span style="user-select:none;color:var(--color);padding-bottom:20px">{{name}}</span>
                    <i id="skillIcon" style="color:var(--color)" :class="icon"></i>
                </div>
            </div>
</template> 

<script>

export default {
    props:['name','icon']
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