<template>
    <header>
        <!-- Header navBar -->
        <nav class="navbar navbar-expand-lg">
            <div class="container-fluid">
                <a class="navbar-brand" href="#"><img src="../assets/img/logo-light.png" alt="icamedy Logo"></a>
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item text-uppercase" 
                    v-for="(item, index) in navItems" 
                    :key="index">
                    <a class="nav-link text-white" :href="item.link">{{item.text}} </a>
                    </li>
                </ul>
            </div>
        </nav>
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
                    text: 'symbols',
                    link: '#'
                },
                
            ] 
        }
    }
}
</script>

<style lang="scss" scoped>
header{
    width:100%;
    position:fixed;
    top:0;
}
</style>