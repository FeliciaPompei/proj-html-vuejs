<template>
    <main>
        <Slider 
        :element = "topSlider"
        />
        <NavBar
        :schoolSubjects = "schoolSubjects"
        />
        <Course/>
        <SliderReviews
        :sliderReviews ='sliderReviews'
        />

        <!-- slider Review -->
        <!-- slider vertical-->
        <!-- slider -->
        <!-- pricing plans  -->
        <!-- similar to mini navbar -->
    </main>
</template>

<script>
import Slider from './Slider.vue'
import NavBar from './NavBar.vue'
import Course from './Course.vue'
import SliderReviews from './SliderReviews.vue'
export default {
    name: 'MainIndex',
    components :{
        Slider,
        NavBar,
        Course,
        SliderReviews
    },
    data(){
        return{
            // Top Slider Info
            topSlider:[
                {
                    id : 'slider-1',
                    image : 'h6-slide-1-background.jpg',
                    title: 'Leaders in Learning',
                    subTitle : 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    buttonText : 'register now',
                    link: '#',
                    class : 'my-circle'
                },
                {   
                    id : 'slider-2',
                    image : 'h5-slide-1-background.jpg',
                    title: 'Accelerate Your Career',
                    subTitle : 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    buttonText : 'register now',
                    link: '#',
                    class : 'my-circle'
                },
                {
                    id : 'slider-3',
                    image : 'course-9-f-img.jpg',
                    title: 'Contemporary Ideas',
                    subTitle : 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    buttonText : 'register now',
                    link: '#',
                    class : 'my-circle'
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
            sliderReviews : [
                {
                    id: 1,
                    avatar: 'testimonials-standard-1.png',
                    comment:'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    name:'Bubble Gum Girl',
                    status:'student',
                    class : 'my-circle'
                },
                {
                    id: 2,
                    avatar: 'testimonials-standard-2.png',
                    comment:'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    name:'Joan Collins',
                    status:'student',
                    class : 'my-circle'
                },
                {
                    id: 3,
                    avatar: 'testimonials-standard-3.png',
                    comment:'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    name:'I look smart cause I\'m wearing glasses',
                    status:'teacher',
                    class : 'my-circle'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
main{
    background-color: palevioletred;
}
</style>
