<template>
  <div id="resumeCard" class="shadow-lg px-5 py-4 my-5">
    <div class="d-flex mb-4 justify-content-between">
        <a id="blue" class="h4 text-decoration-underline" :href="link" target="_blank">{{name}}</a>
        <h5 id="colorText">{{date}}</h5>
    </div>
    <p id="colorText">{{message}}</p>
    <div class="d-flex justify-content-center align-items-center">
        <img class="img-fluid" :src="img" :alt="name">
    </div>
</div>

</template>

<script>
export default {
    props:["name","message","date","img","link"]
}
</script>

<style scoped>

#blue{
    color:var(--color)
}

#colorText{
    color:var(--text-color)
}

</style>