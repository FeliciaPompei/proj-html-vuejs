<template>
    <main>
        <Slider/>
        <!-- slider -->
        <!-- mini nav bar -->
        <!-- info about course with button on go to the top of the page-->
        <!-- slider -->
        <!-- info about course with button on go to the top of the page-->
        <!-- slider -->
        <!-- pricing plans  -->
        <!-- similar to mini navbar -->
    </main>
</template>

<script>
import Slider from './Slider.vue'
export default {
    name: 'MainIndex',
    components :{
        Slider,
    }
}
</script>

<style lang="scss" scoped>
main{
    height: 150vh;
    background-color: palevioletred;
}
</style>