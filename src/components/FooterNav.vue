<template>
    <section class="container-fluid p-3">
        <div class="row justify-content-evenly">
            <div class="col-4 d-flex flex-column"
            v-for="(contact, index) in footerConctacts"
            :key="index">
                <img src="`img/${contact.logo}.png`" alt="Iacamedy Logo">
                <span>
                    {{contact.pharse}}
                </span>
                <span>
                    <i class="fas fa-phone"> </i>
                    {{contact.phoneNumber}}
                </span>
                <span>
                    <i class="fas fa-clock"> </i>
                    {{contact.openingDays}}
                </span>
            </div>
            <div class="col-4"
            v-for="(link, index) in footerLinks"
            :key="index">
            <h2>{{link.title}} </h2>
                <ul>
                    <li
                    v-for="(element, index) in footerLinks[index].links"
                    :key="index" >
                        {{element.text}}
                        {{element.link}}
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
}
</style>