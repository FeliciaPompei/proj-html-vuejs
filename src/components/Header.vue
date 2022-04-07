<template>
    <header>
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <div class="container-fluid">
                <a class="navbar-brand" href="#">Logo</a>
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item text-uppercase" 
                    v-for="(item, index) in navItems" 
                    :key="index">
                    <a class="nav-link active" :href="item.link">{{item.text}} </a>
                    </li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'HeaderIndex',
    data(){
        return{
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
    position:fixed;
    top:0;
}
</style>