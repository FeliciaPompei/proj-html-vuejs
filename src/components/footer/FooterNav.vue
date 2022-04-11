<template>
    <section class="container-fluid py-5 text-white">
        <div class="row justify-content-evenly">
            <div class="col-3 d-flex flex-column"
            v-for="(contact, index) in footerConctacts"
            :key="index">
                <img id="logo"
                class="mb-5"
                :src="`img/${contact.logo}`"
                alt="Iacamedy Logo">
                <span class="pe-5 mb-4">
                    {{contact.pharse}}
                </span>
                <span class="mb-3">
                    <i class="fas fa-phone"> </i>
                    {{contact.phoneNumber}}
                </span>
                <span>
                    <i class="fas fa-clock"> </i>
                    {{contact.openingDays}}
                </span>
            </div>
            <div class="col-3"
            v-for="(link, index) in footerLinks"
            :key="index">
            <h2 class="mb-5">
                {{link.title}}
            </h2>
                <ul class="list-group">
                    <li class="mb-3"
                    v-for="(element, index) in footerLinks[index].links"
                    :key="index" >
                        <h6 class="mb-0 fw-bold">
                            {{element.text}}
                        </h6>
                        {{element.link}}
                        <div v-if="element.img">
                            <img id="footer-img"
                            class="img-fluid"
                            :src="`img/${element.img}`" 
                            alt="world map">
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name:'footerNavBar',
    props: ['footerConctacts', 'footerLinks'],
    data : function(){
        return{
            list:0,
        }
    },
    methods: {
        displayListItems(index){
            if(index > -1){
                this.list = index;
            }
        },
    }
}
</script>

<style lang="scss" scoped>
section {
    border-bottom: 1px white solid;
    width:90%;
    #logo{
        width: 150px;
    }
    ul{
        li{
        list-style: none;
        }
    }
}
</style>