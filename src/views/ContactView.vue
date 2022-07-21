<template>
  <div class="contact">
    <div class="container d-flex justify-content-center flex-column min-vh-100">
            <h4 id="blueColor" class="my-1 display-1">Contact</h4>
            <h6 id="blueColor" class="fs-5">Send me a message</h6>
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
    border-color: var(--color);
    color: var(--color);
    font-weight: 900;
    background-color: transparent;
    border: 0.188rem solid var(--color);
    transition: all 0.2s ease-in-out;
}

.hoverButton:hover {
    background-color: var(--color);
    color: white;
}

#contactIcon{
    position: absolute;
    top: 1.563rem;
    right: 1.25rem;
}

#blueColor{
    color:var(--color)
}

:placeholder{
    color:var(--text-color)
}

#inputContainer{
    position: relative;
}

.form-control{
    border-radius: 0%;
    border-bottom: var(--border) solid var(--color);
}

</style>