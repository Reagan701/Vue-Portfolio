<template>
  <div class="contact">
    <div id="paddingLeft" class="container vh-100 d-flex flex-column justify-content-center align-items-center my-5 text-center">
            <h4 class="mt-1 fs-1">Contact</h4>
            <h6 class="fs-6">Get in touch</h6>
            <form action="https://formspree.io/f/xayvrbqy" method="POST" class="w-100 my-5 py-5 mx-auto">
                <div class="row">
                    <div class="col-md-4">
                        <div id="inputContainer" class="col-md-12">
                            <input type="text" name="name" placeholder="Enter your Full Name" class=" py-4 form-control" required>
                            <label for="name">
                                <i id="contactIcon" class="bi bi-person"></i>
                            </label>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div id="inputContainer" class="col-md-12">
                            <input type="email" name="email" placeholder="Enter your Email" class="py-4 form-control" required>
                            <label for="email">
                                <i id="contactIcon" class="bi bi-envelope"></i>
                            </label>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div id="inputContainer" class="col-md-12">
                            <input type="text" name="subject" placeholder="Enter your Subject" class="py-4 form-control" required>
                            <label for="subject">
                                <i id="contactIcon" class="bi bi-check2-square"></i>
                            </label>
                        </div>
                    </div>
                </div>
                <div class="row mt-5">
                    <div id="inputContainer" class="col-md-12">
                        <textarea type="text" name="message" placeholder="Send me a message" class="py-4 form-control"></textarea>
                        <label for="message"> <i id="contactIcon" class="bi bi-pencil-square"></i> </label>
                    </div>
                </div>
                <div class="row mt-5 text-start">
                    <div class="col-md-12">
                        <button type="submit" class="hoverButton p-4"> Send Now! </button>
                    </div>
                </div>
            </form>
        </div>
  </div>
</template>

<script>

export default {

}
</script>

<style scoped>

.hoverButton{
    border-color: #190844;
    color: #190844;
    font-weight: 900;
    background-color: transparent;
    border: 0.188rem solid #190844;
    transition: all 0.2s ease-in-out;
}

.hoverButton:hover {
    background-color: #190844;
    color: white;
}

#contactIcon{
    position: absolute;
    top: 1.563rem;
    right: 1.25rem;
}

#inputContainer{
    position: relative;
}

.form-control{
    border-radius: 0%;
    border:0.2rem solid var(--color)
}

</style>