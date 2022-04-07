<template>
    <nav class="container">
        <div class="row">
            <div class="col-2"
            v-for="(element, index) in schoolSubjects"
            :key="index"
            >
            <img :src="`img/${element.image} `" :alt="element.text">
            <h6>
                {{element.text}} 
            </h6>
            </div>
        </div>
        
    </nav>
</template>

<script>
export default {
    name:'NavBar',
    props : ['schoolSubjects'],
}
</script>

<style lang="scss" scoped>
    nav{
        height:10vh;
        background-color: palegreen;
    }
</style>