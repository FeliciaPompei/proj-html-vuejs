<template>
    <section class="container-fluid p-5 d-flex">
        <div class="thumbnails p-3">
            <ul
            v-for="(thumbnail, index) in aboutIcademy"
            :key="thumbnail.id"
            @click="displayListItems(index)">
                <li class="thumbnail p-3"
                @click="questionClick(index)"
                :class="(index == sliderIndex) ? 'my-active fw-bold' : ''">
                    {{thumbnail.question}}
                </li>
            </ul>
        </div>
        <div class="article p-5">
            <div class="mb-5"
            v-for="(element, index) in aboutIcademy"
            :key="index"
            :class="(index == sliderIndex) ? 'd-block' : 'd-none' ">
                <h1 class="mb-3">
                    {{element.title}}
                </h1>
                <p class="mb-3 text-secondary">
                    {{element.content}}
                </p>
            </div>
            <div class="d-flex">
                <div>
                    <ul class="p-0">
                        <li class="my-check-mark"
                        v-for="(item, index) in aboutIcademy[listIndex].list"
                        :key="index">
                            {{item.item}}
                        </li>
                    </ul>
                </div>
                <div class="align-self-end ms-5" 
                v-for="(element, index) in aboutIcademy"
                :key="index"
                :class="(index == sliderIndex) ? 'd-block' : 'd-none' ">
                    <img class="img-fluid" 
                    :src="`img/${element.image}`" 
                    alt="Symbol">
                </div>
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
            listIndex : 0,
        }
    },
    methods:{
        displayListItems(index){
            if(index > -1){
                this.listIndex = index;
            }
        },
        questionClick: function(imageIndex){
            this.sliderIndex = imageIndex;
        },
    }
}
</script>

<style lang='scss' scoped>
section{
    // background-color:paleturquoise;
    // height:100vh;
    .thumbnails{
        width:30%;
        // background-color: palegreen;
        .thumbnail{
            list-style: none;
        }
    }
    .my-active{
        border-left: #40C4FF solid 5px;
        color:#40C4FF;
    }
    .article{
        width:70%;
        // background-color: palevioletred;
    }
    .my-check-mark:before{
        content:'\2713';
        font-size: 1.5rem;
        color:lightblue;
    }
    .my-check-mark{
        list-style:none;
        padding: 0.5rem;
        padding-left:0;
    }
}
</style>