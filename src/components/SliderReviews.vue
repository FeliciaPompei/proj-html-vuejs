<template>
    <div>
        <div class="my-slider-container d-flex justify-content-center mb-5"
        @mouseleave = "autoPlay" 
        @mouseover = "stopPlay">
            <div class="d-flex flex-column justify-content-center align-items-center my-content-box"
            v-for="(review, index) in sliderReviews" 
            :key="index"
            :class="(index == sliderIndex) ? 'd-block' : 'd-none' "> 
                <img class="card-img-top rounded-circle mb-3"  :src="`img/${review.avatar}`" :alt="review.name" >
                <div class="img-description p-3 text-center">
                    <p> 
                        {{review.comment}} 
                    </p>
                    <h5> 
                        {{review.name}}
                    </h5>
                    <h6> 
                        {{review.status}} 
                    </h6>
                </div>
            </div>
            <div class="buttons text-white">
                <div class= "my-circle-wrapper">
                        <div
                        v-for="(review, index) in sliderReviews"
                        :key="index"
                        @click="imageClick(index)" 
                        class="me-2"
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
.my-slider-container {
    width:100%;
    height:60vh;
    background-color: green;
    position:relative;
    padding:2rem;
    // background-image: url(img/h5-parallax-img-1.png);
    .my-content-box{
        width:50%;
        color:white;

        img{
        width:150px;
        height:150px;
        object-fit: cover;
        }
        h1{
            font-size: 4rem;
            color:white;
            background-color: rgba($color: #000000, $alpha: 0.4);
            border-radius: 2rem;
            padding: 1rem;
        }

    }
    .my-circle-wrapper{
        display:flex;
        position: absolute;
        bottom:2rem;
        left:50%;
        transform: translateX(-50%);
        // background-image:url(./public/img/h5-parallax-img-1.png);

        #my-circle{
            display:block;
            width:20px;
            height:20px;
            border-radius: 50%;
            background-color:gray;
        }

        .active{
            background-color:white;
            border: 5px solid white;
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