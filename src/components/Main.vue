<template>
    <main class="position-relative">
        <Slider 
        :element = "topSlider"
        />
        <NavBar
        :schoolSubjects = "schoolSubjects"
        />
        <div class="top-button course p-2">
            <a class="text-uppercase text-white" 
            href="#"> 
                <i class="fas fa-chevron-up text-center"> top </i>
            </a>
        </div>
        <Course/>
        <div class="top-button art-empowering p-2">
            <a class="text-uppercase text-white" 
            href="#"> 
                <i class="fas fa-chevron-up text-center"> top </i>
                
            </a>
        </div>
        <div class="top-button slider-review p-2">
            <a class="text-uppercase text-white" 
            href="#"> 
                <i class="fas fa-chevron-up text-center"> top </i>
                
            </a>
        </div>
        
        <SliderReviews
        :sliderReviews ='sliderReviews'
        />
        <LearningSection
        :aboutIcademy ='aboutIcademy'
        />

        <OnlineCoursesSlider
        :onlineCourses = 'onlineCourses'
        />
        <PriceList/>
        
        <!-- similar to mini navbar -->
    </main>
</template>

<script>
import Slider from './Slider.vue'
import NavBar from './NavBar.vue'
import Course from './Course.vue'
import SliderReviews from './SliderReviews.vue'
import LearningSection from './LearningSection.vue'
import OnlineCoursesSlider from './OnlineCourseSlider.vue'
import PriceList from './PriceList.vue'
export default {
    name: 'MainIndex',
    components :{
        Slider,
        NavBar,
        Course,
        SliderReviews,
        LearningSection,
        OnlineCoursesSlider,
        PriceList
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
            ],
            aboutIcademy : [
                {
                    question : 'What We Do',
                    title: 'Learning Possibilities',
                    content: 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    image:'h3-custom-icon-1.png',
                    list :[
                        {
                            item :'Maximizing potential throught individual attention',
                        },
                        {
                            item :'The trusted name for specialized training',
                        },
                        {
                            item :'The trusted name for specialized training.'
                        },
                        {
                            item :'People teach. People learn. This is where they connect.'
                        }
                    ]
                },
                {
                    question : 'Degree Programme',
                    title: 'The Degree we provide',
                    content: 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    image:'h3-custom-icon-2.png',
                    list :[
                        {
                            item :'Maximizing potential throught individual attention',
                        },
                        {
                            item :'The trusted name for specialized training',
                        },
                        {
                            item :'The trusted name for specialized training.'
                        },
                        {
                            item :'People teach. People learn. This is where they connect.'
                        }
                    ]
                },
                {
                    question : 'Career Archievements',
                    title: 'Career Archievements',
                    content: 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    image:'h3-custom-icon-3.png',
                    list :[
                        {
                            item :'Maximizing potential throught individual attention',
                        },
                        {
                            item :'The trusted name for specialized training',
                        },
                        {
                            item :'The trusted name for specialized training.'
                        },
                        {
                            item :'People teach. People learn. This is where they connect.'
                        }
                    ]
                },
                {
                    question : 'Personal Managment',
                    title: 'Personal Managment',
                    content: 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    image:'h3-custom-icon-4.png',
                    list :[
                        {
                            item :'Maximizing potential throught individual attention',
                        },
                        {
                            item :'The trusted name for specialized training',
                        },
                        {
                            item :'The trusted name for specialized training.'
                        },
                        {
                            item :'People teach. People learn. This is where they connect.'
                        }
                    ]
                },
                {
                    question : 'Steps To Success',
                    title: 'Steps To Success',
                    content: 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    image:'h3-custom-icon-5.png',
                    list :[
                        {
                            item :'Maximizing potential throught individual attention',
                        },
                        {
                            item :'The trusted name for specialized training',
                        },
                        {
                            item :'The trusted name for specialized training.'
                        },
                        {
                            item :'People teach. People learn. This is where they connect.'
                        }
                    ]
                },
                {
                    question : 'Knowledge Transfer',
                    title: 'Knowledge Transfer',
                    content: 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh id elited odio sit amet nibcursus a sit amet mauris.',
                    image:'h3-custom-icon-6.png',
                    list :[
                        {
                            item :'Maximizing potential throught individual attention',
                        },
                        {
                            item :'The trusted name for specialized training',
                        },
                        {
                            item :'The trusted name for specialized training.'
                        },
                        {
                            item :'People teach. People learn. This is where they connect.'
                        },
                    ]
                }
            ],
            onlineCourses : [
                [
                    {   
                    image:'course-1-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'lorem',
                    group: 1,
                    courseType: 'programming',
                    class : 'my-circle'
                },
                {
                    image:'course-2-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'lorem',
                    group: 1,
                    courseType: 'business',
                    class : 'my-circle'
                },
                {
                    image:'course-3-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'lorem',
                    group: 1,
                    courseType: 'business',
                    class : 'my-circle'
                }
                ],
                [
                    {
                    image:'course-4-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'$120',
                    content: 'lorem',
                    group: 2,
                    courseType: 'business',
                    class : 'my-circle'
                },
                {
                    image:'course-5-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'$50',
                    content: 'lorem',
                    group: 1,
                    courseType: 'programming',
                    class : 'my-circle'
                },
                {
                    image:'course-6-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'lorem',
                    group: 1,
                    courseType: 'programming',
                    class : 'my-circle'
                }
                ],
                [
                    {
                    image:'course-7-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'lorem',
                    group: 2,
                    courseType: 'business',
                    class : 'my-circle'
                },
                {
                    image:'course-8-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'lorem',
                    group: 1,
                    courseType: 'programming',
                    class : 'my-circle'
                },
                {
                    image:'course-9-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'$20',
                    content: 'lorem',
                    group: 1,
                    courseType: 'programming',
                    class : 'my-circle'
                }
                ]
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.top-button{
    background-color: #40C4FF;
    width: 50px;
    height:50px;

    position:absolute;
    right:0;
}
.course{
    top:37%;
}
.art-empowering{
    top: 59%;
}
.slider-review{
    top:71%;
}
</style>
