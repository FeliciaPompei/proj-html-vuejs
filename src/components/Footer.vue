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
import FooterNav from './FooterNav.vue'
import FooterBot from './FooterBot.vue'
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
                    logo:'h5-client-1',
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
                            link:'img'
                        }
                    ]
                }
                
            ],
            socialMedia :[
                {
                    text:'Twitter',
                    img:'',
                },
                {
                    text:'Instragram',
                    img:'',
                },
                {
                    text:'FaceBook',
                    img:'',
                },
            ]
        }
        
    }
}
</script>

<style lang="scss" scoped>
    footer{
        background-color: gray;
    }
</style>