<template>
<!-- Add button to go to the top -->
    <section class="container-fluid pt-5">
        <div class="row p-5">
            <div class="col-6 px-5">
                <h1 class="fw-bold my-title-size mb-3">
                    The Trusted Name for In-Home Tutoring.
                </h1>
            </div>
            <div class="col-12 px-5">
                <p class="fs-5">
                    Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.
                </p>
                <a class="text-uppercase text-info text-decoration-none fw-bold"
                href="#" >
                    learn more
                </a>
            </div>
            
            <div class="col-12 d-flex justify-content-center position-relative">
                <img 
                src="img/h5-img-1.jpg" 
                alt="Teenagers readings and smiling">
            </div>
            
        </div>
        <div class="row justify-content-center align-items-center p-5 position-relative">
            <div class="col-6 p-5">
                <img 
                src="img/blog-post-12-550x550.jpg" 
                alt="Hands holding the world">
            </div>
            <div class="col-6 p-5 position-relative">
                <h1 class="fw-bold my-title-size mb-3">
                    Empowering Children to Reach Their Potential.
                </h1>
                <p class="fs-6 text-secondary">
                    Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.
                </p>
                <div class="row my-text-color">
                    <div class="col-6">
                        <h1 class="my-title-size fw-bold">
                            168
                        </h1>
                        <h5>
                            User Stories
                        </h5>
                    </div>
                    <div class="col-6">
                        <h1 class="my-title-size fw-bold">
                            347
                        </h1>
                        <h5>
                            Events
                        </h5>
                    </div>
                </div>
                
            </div>
            <div class="top-button course p-2">
                <a class="text-uppercase text-white" 
                href="#"> 
                    <i class="fas fa-chevron-up text-center"> top </i>
                </a>
            </div>
        </div>
        
    </section>
</template>

<script>
export default {
    name:'CouseInformation',
}
</script>

<style lang="scss" scoped>
@import "../../assets/styles/partials/_variables.scss";
.container{
    position:relative;
}
.my-title-size{
    font-size:3rem;
}
.my-text-color{
    color:$lightBlueColor;
}
.top-button{
    background-color: $lightBlueColor;
    width: 50px;
    height:50px;

    position:absolute;
    right:0;
    top:50%;

}
</style>