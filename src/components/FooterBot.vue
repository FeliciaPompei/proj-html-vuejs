<template>
    <section class="container-fluid p-3">
        <div class="row">
            <div class="col-6">
                <span>Copyrights 2017 <i></i>Mikado Themes</span>
            </div>
            <div class="col-6 d-flex">
                <p>CALL +44 300 303 0266</p>
                <p>follow us</p>
                <div
                v-for="(link, index) in socialMedia"
                :key="index">
                    <img :src="`img/${link.img} `" :alt="link.text">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name:'footerBottom',
    props:['socialMedia'],
}
</script>

<style lang="scss" scoped>

</style>