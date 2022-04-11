<template>
    <section class="container-fluid p-4">
        <div class="row pt-4">
            <div class="col-12 text-center mb-5">
                <h1 class="mb-3">
                    Popular Online Courses
                </h1>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi ab commodi numquam reiciendis excepturi
                </p>
            </div>
        </div>
        <div class="slider-container" 
        @mouseleave="autoPlay" 
        @mouseover="stopPlay">
            <div class="my-slider-cards d-flex p-5">
                <div 
                v-for="(sliderElement, index) in onlineCourses[pageNumber]" 
                :key="index"
                >
                    <div class="justify-content-center align-items-center p-3 mb-2">
                        <img class="card-img-top w-100 d-block"
                        :src="`img/${sliderElement.image}.jpg`" 
                        :alt="sliderElement.type">
                        <div class="card-body w-100">
                            <div class="d-flex justify-content-between mb-2">
                                <div>
                                    <h5 class="card-title mb-1">
                                        {{sliderElement.type}}
                                    </h5>
                                    <span class="text-secondary">
                                        {{sliderElement.teacher}}
                                    </span>
                                </div>
                                <span class="rounded-pill text-white my-price-tag align-self-start"
                                :class="(sliderElement.price == 'free') ? 'bg-warning' : 'bg-info'"> 
                                    {{sliderElement.price}} 
                                </span>
                            </div>
                            <p class="card-text text-secondary pe-5">
                                {{sliderElement.content}}
                            </p>
                            <span class="text-secondary me-2">
                                <i class="fas fa-user me-1"></i> 
                                {{sliderElement.group}}
                            </span>
                            <span class="text-secondary">
                                <i class="fas fa-tag me-1"></i> 
                                {{sliderElement.courseType}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class= "my-circle-wrapper">
                    <div
                    v-for="(sliderElement, index) in onlineCourses[pageNumber]"
                    :key="index"
                    @click="displayListItems(index)" 
                    class="me-2 my-bg-color"
                    :class="sliderElement.class">
                    </div>
                </div>
            </div>
        </div>
        <div class="top-button course p-2">
                <a class="text-uppercase text-white" 
                href="#"> 
                    <i class="fas fa-chevron-up text-center"> top </i>
                </a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'OnlineCoursesSlider',
    props : ['onlineCourses'],
    data(){
        return {
            isInAutoScroll : null,
            sliderIndex : 0,
            pageNumber : 0,
        }
    },
    methods : {
        displayListItems(index){
            if(index > -1){
                this.pageNumber = index;
            }
        },
        imageClick: function(imageIndex){
            this.sliderIndex = imageIndex;
        },
        nextSlide : function (){
            if(this.sliderIndex == (this.onlineCourses.length -1)){
                this.sliderIndex = 0;
            } else {
                this.sliderIndex++;
            }
        },
        previousSlide : function (){
            if(this.sliderIndex == 0){
                this.sliderIndex = this.onlineCourses.length -1;
            } else {
                this.sliderIndex--;
            }
        },
        autoPlay : function(){
            this.isInAutoScroll = setInterval(this.nextSlide, 3000);
        },
        stopPlay: function(){
            this.isInAutoScroll = clearInterval(this.isInAutoScroll);
            this.isInAutoScroll = null;
        },
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/styles/partials/_variables.scss";
section{
    position:relative;

}
.slider-container {
    width:100%;
    height:68vh;
    position:relative;
    margin-bottom:7rem;
    
.my-circle-wrapper{
        display:flex;
        position: absolute;
        bottom:-5rem;
        left:50%;
        transform: translateX(-50%);

        .my-circle{
            display:block;
            width:15px;
            height:15px;
            border-radius: 50%;
            
        }
        .my-bg-color{
            background-color:$circleBg;
        }

        .active{
            background-color:white;
        }
        
    }
    .fa-tag, .fa-user, .my-price-tag{
            font-size: 0.7rem;
        }
        .my-price-tag{
            padding: 0.2rem 0.5rem;
            
        }
}
</style>