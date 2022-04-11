<template>
    <section>
        <div class="container p-5">
            <div class="row">
                <div class="col-3 mb-3 p-2"
                v-for="(element, index) in sponsoreShips"
                :key="index">
                    <img :src="`img/${element.img}.png`" alt="img">
                </div>
            </div>
        </div>
        <div class="top-button course p-2">
                <a class="text-uppercase text-white" 
                href="#"> 
                    <i class="fas fa-chevron-up text-center"> top </i>
                </a>
        </div>
    </section>
</template>

<script>
export default {
    name:'sponsoreShips',
    props:['sponsoreShips'],

}
</script>

<style lang="scss" scoped>

section{
    position:relative;
}
</style>