<template>
    <nav class="container mb-5">
        <div class="row">
            <div class="col-2 d-flex justify-content-center"
            v-for="(element, index) in schoolSubjects"
            :key="index"
            >
                <div class="my-content-container">
                    <img class="mb-3"
                    :src="`img/${element.image} `" 
                    :alt="element.text">
                    <h6 class="text-center">
                        {{element.text}} 
                    </h6>
                </div>
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
        .my-content-container{
            background-color:#D6F2FF;
            padding:3rem 2.5rem;
        }
        img{
            // width:150px;
            // height:150px;

        }
        h6 {
            
        }
    }
</style>