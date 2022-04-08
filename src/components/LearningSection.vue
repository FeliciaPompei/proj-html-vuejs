<template>
    <section class="container-fluid p-5 d-flex">
        <ul class="thumbnails p-3 d-flex flex-column"
        v-for="(thumbnail, index) in aboutIcademy"
        :key="thumbnail.id">
            <li class="thumbnail"
            @click="questionClick(index)">
                {{thumbnail.question}}
            </li>
        </ul>
        <div 
        v-for="(element, index) in aboutIcademy"
        :key="index"
        :class="(index == sliderIndex) ? 'd-block' : 'd-none' "
        >
            <div class="article p-3"
            >
                <h1>
                    {{element.title}}
                </h1>
                <p>
                    {{element.content}}
                </p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name:'LearningSection',
    props:['aboutIcademy'],
    data(){
        return{
            sliderIndex : 0,
        }
    },
    methods:{
        questionClick: function(imageIndex){
            this.sliderIndex = imageIndex;
        },
    }
}
</script>

<style lang='scss' scoped>
section{
    background-color:paleturquoise;
    height:100vh;
    .thumbnails{
        width:30%;
        background-color: palegreen;
        .thumbnail{
            border: 1px solid black;
        }
    }
    .article{
        width:70%;
        background-color: palevioletred;
    }
}
</style>