<template>
    <section class="container-fluid p-5 text-white">
        <div class="row justify-content-between">
            <div class="col-6">
                <span>Copyrights 2017 <i class="fa fa-copyright pe-1"> </i>Mikado Themes</span>
            </div>
            <div class="col-4 d-flex justify-content-evenly text-uppercase">
                <p>
                    call +44 300 303 0266
                </p>
                <p>
                    follow us
                </p>
                <div
                v-for="(link, index) in socialMedia"
                :key="index">
                    <i :class="link.icon"></i>
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