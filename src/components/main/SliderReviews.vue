<template>
    <div>
        <div class="my-slider-container d-flex justify-content-center mb-5"
        @mouseleave = "autoPlay" 
        @mouseover = "stopPlay">
            <div class="d-flex flex-column justify-content-center align-items-center my-content-box"
            v-for="(review, index) in sliderReviews" 
            :key="index"
            :class="(index == sliderIndex) ? 'd-block' : 'd-none' "> 
                <img class="card-img-top rounded-circle mb-3"
                :src="`img/${review.avatar}`" 
                :alt="review.name" >
                <div class="img-description p-3 text-center">
                    <h5 class="mb-4"> 
                        {{review.comment}} 
                    </h5>
                    <h5 class="fw-bold"> 
                        {{review.name}}
                    </h5>
                    <p class="text-uppercase fw-bold"> 
                        {{review.status}} 
                    </p>
                </div>
            </div>
            <div class="buttons text-white">
                <div class= "my-circle-wrapper">
                        <div
                        v-for="(review, index) in sliderReviews"
                        :key="index"
                        @click="imageClick(index)" 
                        class="me-2 my-bg-color"
                        :id="review.class"
                        :class="(index == sliderIndex) ? 'active' : ''">
                        </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SliderReviews',
    props : ['sliderReviews'],
    data(){
        return {
            isInAutoScroll : null,
            sliderIndex : 0
        }
    },
    methods : {
        nextSlide : function (){
            if(this.sliderIndex == (this.sliderReviews.length -1)){
                this.sliderIndex = 0;
            } else {
                this.sliderIndex++;
            }
        },
        previousSlide : function (){
            if(this.sliderIndex == 0){
                this.sliderIndex = this.sliderReviews.length -1;
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
        imageClick: function(imageIndex){
            this.sliderIndex = imageIndex;
        },
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/styles/partials/_variables.scss";

.my-slider-container {
    width:100%;
    height:80vh;
    position:relative;
    padding:2rem;
    background-image: url("../../../public/img/h5-parallax-img-1.png");
    background-position: center;
    .my-content-box{
        width:50%;
        color:white;

        img{
        width:125px;
        height:125px;
        object-fit: cover;
        }
        h1{
            font-size: 4rem;
            color:white;
            border-radius: 2rem;
            padding: 1rem;
        }

    }
    .my-circle-wrapper{
        display:flex;
        position: absolute;
        bottom:6rem;
        left:50%;
        transform: translateX(-50%);

        #my-circle{
            display:block;
            width:10px;
            height:10px;
            border-radius: 50%;
            
        }
        .my-bg-color{
            background-color: $circleBg;
        }

        .active{
            background-color:white;
        }
    }
    .my-previous, .my-next{
        position: absolute;
        top:50%;
        transform: translateY(-50%);
        cursor: pointer;
        padding: 0.5rem 1rem;
        font-size: 1.5rem;
    }
    .my-previous{
        left: 2rem;
    }
    .my-next{
        right: 2rem;
    }
}
</style>