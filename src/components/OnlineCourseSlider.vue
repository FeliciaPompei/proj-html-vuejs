<template>
    <div class="container">
        <div class="row">
            <div class="col-12 text-center mb-5">
                <h1>Popular Online Courses</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi ab commodi numquam reiciendis excepturi</p>
            </div>
        </div>
        <div class="slider-container" @mouseleave="autoPlay" @mouseover="stopPlay">
            <div class="my-slider-cards d-flex">
                <div 
                v-for="(sliderElement, index) in onlineCourses[pageNumber]" 
                :key="index"
                >
                    <div class="justify-content-center align-items-center p-3 mb-2">
                        <img class="card-img-top w-100"
                        :src="`img/${sliderElement.image}.jpg`" 
                        :alt="sliderElement.type">
                        <div class="card-body w-100">
                            <h5 class="card-title">{{sliderElement.type}}</h5>
                            <p class="card-text">{{sliderElement.content}}</p>
                            <a href="#" class="btn btn-primary">Go somewhere</a>
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
    </div>
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
.slider-container {
    width:100%;
    height:60vh;
    position:relative;
    margin-bottom:7rem;
    
.my-circle-wrapper{
        display:flex;
        position: absolute;
        bottom:0;
        left:50%;
        transform: translateX(-50%);

        .my-circle{
            display:block;
            width:20px;
            height:20px;
            border-radius: 50%;
            
        }
        .my-bg-color{
            background-color:#9CE0FF;
        }

        .active{
            background-color:white;
        }
    }
}
</style>