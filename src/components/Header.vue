<template>
    <header class="container-fluid d-flex justify-content-center">
        <nav class="navbar navbar-expand-lg">
            <a class="navbar-brand" href="#"><img src="img/logo-light.png" alt="icamedy Logo"></a>
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item text-uppercase m-4" 
                v-for="(item, index) in navItems" 
                :key="index">
                <a class="nav-link text-white"
                :href="item.link"
                v-if="item.text !=''"
                >
                    {{item.text}} 
                </a>
                <a class="nav-link text-white"
                :href="item.link"
                v-else
                >
                <i :class="item.symbol"></i>
                </a>
                </li>
            </ul>
        </nav>
        <!-- Header navBar -->
        
        <!-- /Header navbar -->
    </header>
</template>

<script>
export default {
    name: 'HeaderIndex',
    data(){
        return{
            // navbar items
            navItems : [
                {
                    text: 'home',
                    link: '#'
                },
                {
                    text: 'courses',
                    link: '#'
                },
                {
                    text: 'instructors',
                    link: '#'
                },
                {
                    text: 'events',
                    link: '#'
                },
                {
                    text: 'elements',
                    link: '#'
                },
                {
                    text: '',
                    symbol : 'fas fa-search',
                    link: '#'
                },
                {
                    text: '',
                    symbol : 'fas fa-clipboard',
                    link: '#'
                },
                {
                    text: '',
                    symbol : 'fas fa-bars',
                    link: '#'
                },
                
            ] 
        }
    }
}
</script>

<style lang="scss" scoped>
header{
    position:absolute;
    top:0;
    z-index:3;
    img{
        width:175px;
    }
}
</style>