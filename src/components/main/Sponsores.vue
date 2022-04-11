<template>
    <section class="container p-5">
        <div class="row">
            <div class="col-3 mb-3"
            v-for="(element, index) in sponsoreShips"
            :key="index">
                <img :src="`img/${element.img}.png`" alt="img">
            </div>
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

</style>