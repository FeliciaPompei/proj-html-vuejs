<template>
    <section class="container-fluid p-5 d-flex">
        <div class="thumbnails p-3">
            <ul
            v-for="(thumbnail, index) in aboutIcademy"
            :key="thumbnail.id"
            @click="displayListItems(index)">
                <li class="thumbnail p-4"
                @click="questionClick(index)"
                :class="(index == sliderIndex) ? 'my-active fw-bold' : ''">
                    {{thumbnail.question}}
                </li>
            </ul>
        </div>
        <div class="article p-5">
            <div v-for="(element, index) in aboutIcademy"
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
                    <ul>
                        <li class="my-list-style"
                        v-for="(item, index) in aboutIcademy[listIndex].list"
                        :key="index">
                            {{item.item}}
                            <div class="text-right">
                                <img :src="`img/${item.image} `" alt="">
                            </div>
                        </li>
                    </ul>
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
    .my-list-style{
        list-style: none;
    }
    ul .my-list-style:before{
        content:'\f00cc';
    }
}
</style>