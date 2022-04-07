<template>
    <div>
        <div class="slider-container mb-5" @mouseleave = "autoPlay" @mouseover = "stopPlay">
            <div class="my-slider-images">
                <div> 
                    <!-- Add v-for -->
                    <div class= "img-wrapper">
                        <img class="card-img-top img-fluid"  src="../assets/img/landing-slider-2-img-3.png" :alt="title">
                        <div class="img-description">
                            <h1> title </h1>
                        </div>
                    </div>
                </div>
                <div class="buttons text-white">
                    <div class="my-previous position-absolute">
                        <span class="my-prev-hook"><i class="fa-solid fa-chevron-left"></i></span>
                    </div>
                    <div class="my-next position-absolute">
                        <span class="my-next-hook"><i class="fa-solid fa-chevron-right"></i></span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SliderElement',
    methods : {
        // autoPlay : function(){
        //     this.isInAutoScroll = setInterval(this.nextSlide, 3000);
        // },
        // stopPlay: function(){
        //     this.isInAutoScroll = clearInterval(this.isInAutoScroll);
        //     this.isInAutoScroll = null;
        // },
    }
}
</script>

<style lang="scss" scoped>

</style>