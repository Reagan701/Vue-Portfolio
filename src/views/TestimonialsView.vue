<template>
  <div class="testimonials">
    <div class="container d-flex justify-content-center flex-column min-vh-100">
            <div>
                <h3 id="blueColor" class=" text-center fs-1 my-5"> What people say about me </h3>
            </div>

            <div id="carouselExampleCaptions" class="carousel slide w-100 h-100 d-flex justify-content-center flex-column align-items-center" data-bs-ride="carousel">
                <div class="carousel-indicators">
                    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="bg-dark circle active" aria-label="Slide 1" aria-current="true"></button>
                    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" class="bg-dark circle" aria-label="Slide 2"></button>
                    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" class="bg-dark circle" aria-label="Slide 3"></button>
                </div>
                <div class="carousel-inner h-75">
                    <div class="h-100 w-100 carousel-item active">
                        <div class="d-block d-md-flex gap-5 justify-content-between">
                            <div v-for="testimonial in testimonials.slice(0,2)" :key="testimonial.id" id="Slider">
                                <div class="row m-4">
                                    <div class="col-md-4">
                                        <img id="TestimonialImage" class="img-fluid d-block w-100" :src="testimonial.image" :alt="testimonial.title">
                                    </div>
                                    <div class="col-md-8">
                                        <h2 id="TestimonialName"> {{testimonial.name}}</h2>
                                        <h4 id="TestimonialTitle"> {{testimonial.title}}</h4>
                                    </div>
                                </div>
                                <div class="row m-4">
                                    <p id="TestimonialText">"{{testimonial.message}}"</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="h-100 w-100 carousel-item">
                        <div class="d-block d-md-flex gap-5 justify-content-between">
                            <div v-for="testimonial in testimonials.slice(2,4)" :key="testimonial.id" id="Slider">
                                <div class="row m-4">
                                    <div class="col-md-4">
                                        <img id="TestimonialImage" class="img-fluid d-block w-100" :src="testimonial.image" :alt="testimonial.title">
                                    </div>
                                    <div class="col-md-8">
                                        <h2 id="TestimonialName"> {{testimonial.name}}</h2>
                                        <h4 id="TestimonialTitle"> {{testimonial.title}}</h4>
                                    </div>
                                </div>
                                <div class="row m-4">
                                    <p id="TestimonialText">"{{testimonial.message}}"</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="h-100 w-100 carousel-item">
                        <div class="d-block d-md-flex gap-5 justify-content-between">
                            <div v-for="testimonial in testimonials.slice(4,6)" :key="testimonial.id" id="Slider">
                                <div class="row m-4">
                                    <div class="col-md-4">
                                        <img id="TestimonialImage" class="img-fluid d-block w-100" :src="testimonial.image" :alt="testimonial.title">
                                    </div>
                                    <div class="col-md-8">
                                        <h2 id="TestimonialName"> {{testimonial.name}}</h2>
                                        <h4 id="TestimonialTitle"> {{testimonial.title}}</h4>
                                    </div>
                                </div>
                                <div class="row m-4">
                                    <p id="TestimonialText">"{{testimonial.message}}"</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            testimonials:[
                {
                    id:1,
                    image:'https://i.postimg.cc/h484xYB9/Monique-2.jpg',
                    name: 'Monique Dampies',
                    title:'Colleague, Life Choices',
                    message: "Reagan is a highly skilled individual that would be an asset to any company or team that he is part of. His friendly personality makes him a pleasure to be around. With these qualities, it makes him the best candidate for prospective companies."
                },
                {
                    id:2,
                    image:'https://i.postimg.cc/ZnmT28rB/Emile-3.jpg',
                    name: 'Emile Van Wyk',
                    title:'Colleague, Life Choices',
                    message: "Reagan Carolussen, great attitude, intuitive, Dedicated,Intelligent, these are a few words to describe him. He is a burst of fresh air,easy to talk to and fun loving, he is a diligent individual when it comes to gaining knowledge and applying it proactively, always keeping ahead of the times with a great work ethic and energy for collaboration and assisting others when they need it."
                },
                {
                    id:3,
                    image:'https://i.postimg.cc/4dVfWLhR/Cassidy-1.jpg',
                    name: 'Cassidy Manuel',
                    title:'Colleague, Life Choices',
                    message: "Reagan is a smart, hardworking and fast learner. He has an amazing positive attitude and thrives in a team work environment."
                },
                {
                    id:4,
                    image:'https://i.postimg.cc/L6H9VV9G/Daniel-2.jpg',
                    name: 'Daniel Fredericks',
                    title:'Colleague, Life Choices',
                    message: "Reagan is good at his work and shows a lot of originality with each task. As a colleague it has been inspiring working alongside him and am looking forward to seeing how he will progress in the future. Based on his understanding of the concepts being taught I believe that he has the potential to become a asset for whomever would hire him."
                },
                {
                    id:5,
                    image:'https://i.postimg.cc/6QQ41X9J/joel2.jpg',
                    name: 'Joel Mukanya',
                    title:'Coding Lecturer, Life Choices',
                    message: "I enjoy having Reagan in my class. He demonstrates a fantastic understanding of the materials we are learning in class. Reagan has proven to have an exhaustive understanding of the HTML, CSS &amp; Bootstrap topics we have been studying. Reagan uses his past experience in coding to assist other students. I recommend him."
                },
                {
                    id:6,
                    image:'https://i.postimg.cc/GmdyGDVp/godwin-2.jpg',
                    name: 'Godwin Dzvapatsva',
                    title:'Head of Curriculum and Learning, Life Choices',
                    message: "Reagan has a pleasant personality, which allows him to work with any of his classmates. He submits projects that are well done. I recommend Reagan."
                },
            ]
        }
    }
}
</script>

<style scoped>

#blueColor, #TestimonialName{
  color:var(--color);
}

#TestimonialText{
    color:var(--text-color)
}
#TestimonialTitle{
    color:var(--text-color)
}

    #Slider, #LecturerSlider{
        padding-top:10px;
        width: 100%;
        height: 33rem;
        background-color:rgb(var(--background-color));
        transition: all 0.3s linear;
        box-shadow: var(--shadow);
        border-bottom: var(--border) solid var(--color);

    }

    .carousel-indicators{
        bottom:-80px;
    }
    .circle{
        border-radius: 50%;
        aspect-ratio: 1;
        height: 15px;
        width: 15px;
        background-color:var(--color) !important;
    }

@media screen and (max-width:768px) {
    #Slider, #LecturerSlider{
        height: 55rem;
        background-color:rgb(var(--background-color));
    }
    #TestimonialImage{
        padding: 10px;
        object-fit: cover;
        object-position: top;
    }
}

.carousel-inner{
    overflow: visible;
}

    #TestimonialImage{
        width: 25rem !important;
        max-height: 25rem !important;
        height: 100%;
        object-fit: cover;
        margin-right:auto ;
        margin-left:auto ;
    }
    

    @media screen and (max-width:767px) {
        #testimonialContainer{
            height: 210vh;
        }
    }
    @media screen and (min-width:768px) {
        #testimonialContainer{
            height: 100vh;
        }
    }
    


</style>