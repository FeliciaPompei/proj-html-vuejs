<template>
    <section class="container-fluid p-5 d-flex">
        <div class="thumbnails p-3">
            <ul
            v-for="(thumbnail, index) in aboutIcademy"
            :key="thumbnail.id">
                <li class="thumbnail list-group-item p-4"
                @click="questionClick(index)"
                :class="(index == sliderIndex) ? 'active' : ''">
                    {{thumbnail.question}}
                </li>
            </ul>
        </div>
        <div class="article p-3"
        
        >
            <div v-for="(element, index) in aboutIcademy"
        :key="index"
        :class="(index == sliderIndex) ? 'd-block' : 'd-none' ">
                <h1 class="mb-3">
                    {{element.title}}
                </h1>
                <p class="mb-3">
                    {{element.content}}
                </p>
            </div>
                        <div>
                            <ul>
                    <li
                    v-for="(item, index) in aboutIcademy.list"
                    :key="index">
                        {item}}
                    </li>
                </ul>
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
    // height:100vh;
    .thumbnails{
        width:30%;
        background-color: palegreen;
    }
    .active{
        border-left: blue solid 3px;
        color:blue;
    }
    .article{
        width:70%;
        background-color: palevioletred;
    }
}
</style>