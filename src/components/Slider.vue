<template>
    <div>
        <div class="slider-container" @mouseleave="autoPlay" @mouseover="stopPlay">
            <div class="my-slider-images">
                <div v-for="(sliderElement, index) in element" :key="index"> 
                    <div class="img-wrapper" 
                    :class="(index == sliderIndex) ? 'd-block' : 'd-none' ">
                        <img class="card-img-top img-fluid"
                        :src="`img/${sliderElement.image}`"
                        :alt="sliderElement.title">
                        <div class="img-description">
                            <h1 class="mb-3">
                                {{sliderElement.title}}
                            </h1>
                            <p class="text-white">
                                {{sliderElement.subTitle}}
                            </p>
                            <a class="btn my-custom-btn"
                            :href="sliderElement.link">
                                {{sliderElement.buttonText}}
                            </a>
                        </div>
                    </div>
                </div>
                <div>
                    <div class="my-previous position-absolute" 
                    @click="previousSlide">
                        <span class="my-prev-hook">
                            <i class="fas fa-angle-left"> </i>
                        </span>
                    </div>
                    <div class= "my-circle-wrapper">
                        <div class="me-2 d-flex justify-content-center align-items-center"
                        v-for="(sliderElement, index) in element"
                        :key="index"
                        @click="imageClick(index)" 
                        :id="sliderElement.class"
                        :class="(index == sliderIndex) ? 'active' : ''">
                        <div
                        :class="(index == sliderIndex) ? 'd-block' : 'd-none'">
                            <i class="fas fa-circle"> </i> 
                        </div>
                        </div>
                    </div>
                    <div class="my-next position-absolute" 
                    @click = "nextSlide">
                        <span class="my-next-hook">
                            <i class="fas fa-angle-right"> </i>
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SliderElement',
    props : ['element'],
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
            if(this.sliderIndex == (this.element.length -1)){
                this.sliderIndex = 0;
            } else {
                this.sliderIndex++;
            }
        },
        previousSlide : function (){
            if(this.sliderIndex == 0){
                this.sliderIndex = this.element.length -1;
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
    img{
        width:100%;
        height:85vh;
        object-fit:cover;
        filter: sepia(30%) brightness(0.6);
    }
    .img-description{
        position:absolute;
        top: 50%;
        left:50%;
        transform: translate(-50%, -50%);
        text-align:centeR;
        h1{
            font-size: 4rem;
            color:white;
            border-radius: 2rem;
            padding: 1rem;
        }
        .my-custom-btn{
            padding: 1rem 2.5rem;
            background-color: #40C4FF;
            border-radius: 0;
            text-transform: uppercase;
            color:white;
            font-size: 0.8rem;
        }
    }
    .my-previous, .my-next{
        position: absolute;
        top:50%;
        transform: translateY(-50%);
        cursor: pointer;
        padding: 0.5rem 1rem;
        font-size: 2rem;
    }
    .my-previous{
        left: 2rem;
    }
    .my-next{
        right: 2rem;
    }
    .my-circle-wrapper{
        display:flex;
        position: absolute;
        bottom:2rem;
        left:50%;
        transform: translateX(-50%);

        #my-circle{
            width:20px;
            height:20px;
            border-radius: 50%;
            background-color:#0707071A;

            .fa-circle{
                font-size: 0.5rem;
                text-align: center;
                color:white;
                margin-bottom: 0.6rem;
            }
        }
    }
    .active{
        border:white 2px solid;
        border-radius: 50%;

    }
}
</style>