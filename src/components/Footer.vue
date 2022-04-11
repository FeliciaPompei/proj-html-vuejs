<template>
    <footer>
        <FooterNav
        :footerConctacts ="footerConctacts"
        :footerLinks ="footerLinks"
        />
        <FooterBot
        :socialMedia ="socialMedia"
        />
    </footer>
</template>

<script>
import FooterNav from './footer/FooterNav.vue'
import FooterBot from './footer/FooterBot.vue'
export default {
    name: 'FooterIndex',
    components:{
        FooterNav,
        FooterBot
    },
    data: function(){
        return{
            footerConctacts :[
                {
                    logo:'footer-logo-1.png',
                    pharse:'Providing Life Changing Experiences Through Education. Call That Fot Your Busy Life. Closer to Home',
                    phoneNumber:'1-677-124-44227',
                    openingDays:'Mon-Sat 8:00-18:00'
                }

            ],
            footerLinks : [
                {
                    title:'Popular Courses',
                    links : [
                        {
                            text:'Bunisness English',
                            link:'Preston Marshall'
                        },
                        {
                            text:'Social Computing',
                            link:'David Sanders'
                        },
                        {
                            text:'Learning Spainsh',
                            link:'Jennie King'
                        }
                    ],
                },
                {
                    title:'Support',
                    links:[
                        {
                            link:'User dashboard',
                        },
                        {
                            link:'Contact Us',
                        },
                        {
                            link:'FAQ',
                        },
                        {
                            link:'Course Offer',
                        },
                        {
                            link:'Events',
                        },
                    ],
                },
                {
                    title: 'Flexible Learning',
                    links:[
                        {
                            img:'footer-img-1.png'
                        }
                    ]
                }
                
            ],
            socialMedia :[
                {
                    text:'Twitter',
                    link:'#',
                    icon:'fab fa-twitter',
                },
                {
                    text:'Instragram',
                    link:'#',
                    icon:'fab fa-instagram',
                },
                {
                    text:'FaceBook',
                    link:'#',
                    icon:'fab fa-facebook-f',
                },
            ]
        }
        
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/_variables.scss";

footer{
    background-color: $footerBg;
}
</style>