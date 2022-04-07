<template>
    <main>
        <Slider 
        :element = "topSlider"
        />
        <NavBar
        :schoolSubjects = "schoolSubjects"
        />

        <!-- mini nav bar -->
        <!-- info about course with button on go to the top of the page-->
        <!-- slider -->
        <!-- info about course with button on go to the top of the page-->
        <!-- slider -->
        <!-- pricing plans  -->
        <!-- similar to mini navbar -->
    </main>
</template>

<script>
import Slider from './Slider.vue'
import NavBar from './NavBar.vue'
export default {
    name: 'MainIndex',
    components :{
        Slider,
        NavBar,
    },
    data(){
        return{
            // Top Slider Info
            topSlider:[
                {
                    image : 'h6-slide-1-background.jpg',
                    title: 'Leaders in Learning',
                    subTitle : 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    buttonText : 'register now',
                    link: '#'
                },
                {
                    image : 'h5-slide-1-background.jpg',
                    title: 'Accelerate Your Career',
                    subTitle : 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    buttonText : 'register now',
                    link: '#'
                },
                {
                    image : 'course-9-f-img.jpg',
                    title: 'Contemporary Ideas',
                    subTitle : 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    buttonText : 'register now',
                    link: '#'
                },
            ],
            // NavBar info
            schoolSubjects : [
                {
                    text:'Languages',
                    image:'h5-custom-icon-1.png'
                },
                {
                    text:'Software',
                    image:'h5-custom-icon-2.png'
                },
                {
                    text:'Business',
                    image:'h5-custom-icon-3.png'
                },
                {
                    text:'Chemistry',
                    image:'h5-custom-icon-4.png'
                },
                {
                    text:'Science',
                    image:'h5-custom-icon-5.png'
                },
                {
                    text:'DIY & Craft',
                    image:'h5-custom-icon-6.png'
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
main{
    height: 150vh;
    background-color: palevioletred;
}
</style>
