<template>
    <div>
        <div class="slider-container" @mouseleave="autoPlay" @mouseover="stopPlay">
            <div class="my-slider-cards d-flex">
                <div 
                v-for="(sliderElement, index) in onlineCourses" 
                :key="index"
                :class="(index == sliderIndex) ? 'd-block' : 'd-none'"
                >
                    <div class="card">
                        <img class="card-img-top"
                        :src="`img/${sliderElement.image}.jpg`" 
                        :alt="sliderElement.type">
                        <div class="card-body">
                            <h5 class="card-title">{{sliderElement.type}}</h5>
                            <p class="card-text">{{sliderElement.content}}</p>
                            <a href="#" class="btn btn-primary">Go somewhere</a>
                        </div>
                    </div>
                </div>
                <div class= "my-circle-wrapper">
                    <div
                    v-for="(sliderElement, index) in onlineCourses"
                    :key="index"
                    @click="imageClick(index)" 
                    class="me-2"
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
            sliderIndex : 0
        }
    },
    methods : {
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
    height:85vh;
    position:relative;
    margin-bottom:7rem;
    background-color:palegoldenrod;
    .card{
        width: calc(100% / 3)
    }
    .my-circle-wrapper{
        display:flex;
        position: absolute;
        bottom:2rem;
        left:50%;
        transform: translateX(-50%);

        .my-circle{
            width:20px;
            height:20px;
            border-radius: 50%;
            border: 4px solid lightcoral;
        }
    }
    .active{
        background-color:lightcoral;
    }
}
</style>