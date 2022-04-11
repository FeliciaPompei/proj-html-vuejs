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
                    <a class="text-uppercase"
                    href="#">follow us</a>
                </p>
                <div
                v-for="(link, index) in socialMedia"
                :key="index">
                    <a 
                    :href="link.link">
                        <i :class="link.icon"></i>
                    </a>
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
a{
        text-decoration: none;
        text-transform: none;
        color:white;
    }
    a:hover{
        color:gray;
    }
</style>