<template>
    <main class="position-relative">
        <!-- Banner Slider -->
        <BannerSlider 
        :topSlider = "topSlider"
        />
        <!-- Mini NavBar -->
        <NavBar
        :schoolSubjects = "schoolSubjects"
        />
        <Course/>
        <SliderReviews
        :sliderReviews ='sliderReviews'
        />
        <LearningSection
        :aboutIcademy ='aboutIcademy'
        />

        <OnlineCoursesSlider
        :onlineCourses = 'onlineCourses'
        />
        <PriceList
        :pricingList = 'pricingList'/>
        
        <Sponsores
        :sponsoreShips = 'sponsoreShips'/>
    </main>
</template>

<script>
import BannerSlider from './main/BannerSlider.vue'
import NavBar from './main/NavBar.vue'
import Course from './main/Course.vue'
import SliderReviews from './main/SliderReviews.vue'
import LearningSection from './main/LearningSection.vue'
import OnlineCoursesSlider from './main/OnlineCourseSlider.vue'
import PriceList from './main/PriceList.vue'
import Sponsores from './main/Sponsores.vue'
export default {
    name: 'MainIndex',
    components :{
        BannerSlider,
        NavBar,
        Course,
        SliderReviews,
        LearningSection,
        OnlineCoursesSlider,
        PriceList,
        Sponsores
    },
    data(){
        return{
            // Top Slider Info
            topSlider:[
                {
                    id : 'slider-1',
                    image : 'h6-slide-1-background.jpg',
                    title: 'Leaders in Learning',
                    subTitle : 'Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolLorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dol.',
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
                    subTitle : 'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum auci consequat ipsutis sem nibh.',
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
                    comment:'Lorem Ipsn gravida nibh vel velit auctor aliquetnean, lorem quis bibendum.',
                    name:'Mira Wu',
                    status:'student',
                    class : 'my-circle'
                },
                {
                    id: 2,
                    avatar: 'testimonials-standard-2.png',
                    comment:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem id obcaecati, fuga quaerat molestias maiores a, autem, ea ut corporis asperiores eius dicta neque iusto dolore architecto sunt libero minus!',
                    name:'Joan Collins',
                    status:'student',
                    class : 'my-circle'
                },
                {
                    id: 3,
                    avatar: 'testimonials-standard-3.png',
                    comment:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perferendis, voluptates sequi at animi iste adipisci excepturi, modi dolores, velit ipsam officiis voluptate aperiam. Porro velit ullam odio quo amet officiis',
                    name:'Prof. GreenWood',
                    status:'teacher',
                    class : 'my-circle'
                },
            ],
            aboutIcademy : [
                {
                    question : 'What We Do',
                    title: 'Learning Possibilities',
                    content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perferendis, voluptates sequi at animi iste adipisci excepturi, modi dolores, velit ipsam officiis voluptate aperiam. Porro velit ullam odio quo amet officiis',
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
                    content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perferendis, voluptates sequi at animi iste adipisci excepturi, modi dolores, velit ipsam officiis voluptate aperiam. Porro velit ullam odio quo amet officiis',
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
                    content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perferendis, voluptates sequi at animi iste adipisci excepturi, modi dolores, velit ipsam officiis voluptate aperiam. Porro velit ullam odio quo amet officiis',
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
                    imagehover:'course-10-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis laudantium corrupti corporis nemo ratione.',
                    group: 1,
                    courseType: 'programming',
                    class : 'my-circle'
                },
                {
                    image:'course-2-f-img',
                    imagehover:'course-11-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'$20',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis laudantium corrupti corporis nemo ratione.',
                    group: 1,
                    courseType: 'business',
                    class : 'my-circle'
                },
                {
                    image:'course-3-f-img',
                    imagehover:'course-12-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis laudantium corrupti corporis nemo ratione.',
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
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis laudantium corrupti corporis nemo ratione.',
                    group: 2,
                    courseType: 'business',
                    class : 'my-circle'
                },
                {
                    image:'course-5-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'$50',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis laudantium corrupti corporis nemo ratione.',
                    group: 1,
                    courseType: 'programming',
                    class : 'my-circle'
                },
                {
                    image:'course-6-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis laudantium corrupti corporis nemo ratione.',
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
                    price:'$150',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis laudantium corrupti corporis nemo ratione.',
                    group: 2,
                    courseType: 'business',
                    class : 'my-circle'
                },
                {
                    image:'course-8-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'free',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis laudantium corrupti corporis nemo ratione.',
                    group: 1,
                    courseType: 'programming',
                    class : 'my-circle'
                },
                {
                    image:'course-9-f-img',
                    type: 'Andriod Developer',
                    teacher: 'Davide Sanders',
                    price:'$20',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis laudantium corrupti corporis nemo ratione.',
                    group: 1,
                    courseType: 'programming',
                    class : 'my-circle'
                }
                ]
            ],
            pricingList : [
                {
                    title: 'Save up to 40% byu paying weekly',
                    subject: 'Number of Courses',
                    
                },
                {
                    type: 'Stardard',
                    price: '$12',
                    numberOfCourses : 2,
                    item:'15 Days',
                    webDesigning : 'check',
                    humanCenteredDesign: 'check',
                    basicMarketing:'cross',
                    pythonForEverybody:'cross',
                    androidDeveloper : 'cross',
                    bunsinessEnglish:'cross',
                    button:'get it now'
                },
                {
                    type: 'Professional',
                    price: '$59',
                    numberOfCourses : 4,
                    item:'30 Days',
                    webDesigning : 'check',
                    humanCenteredDesign: 'check',
                    basicMarketing:'check',
                    pythonForEverybody:'check',
                    androidDeveloper : 'cross',
                    bunsinessEnglish:'cross',
                    button:'get it now'
                },
                {
                    type: 'Advanced',
                    price: '$88',
                    numberOfCourses : 6,
                    days:'30 Days',
                    webDesigning : 'check',
                    humanCenteredDesign: 'check',
                    basicMarketing:'check',
                    pythonForEverybody:'check',
                    androidDeveloper : 'check',
                    bunsinessEnglish:'check',
                    button:'get it now'
                }
            ],
            sponsoreShips :[
                {
                    img:'h5-client-5',
                },
                {
                    img:'h5-client-1',
                    
                    
                },
                {
                    img:'h5-client-2',
                },
                {
                    img:'h5-client-4',
                }
            ]
        }
    }
}
</script>

<style lang="scss">
@import "../assets/styles/partials/_variables.scss";
.top-button{
    background-color: $lightBlueColor;
    width: 50px;
    height:50px;
    z-index:3;

    position:absolute;
    right:0;
    top:0;
}
</style>
