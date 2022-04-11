<template>
    <section>
        <div class="container text-center p-5">
            <div class="row">
                <div class="col-12 mb-5">
                    <h1>Pricing Plans</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam magnam molestiae architecto eligendi earum, deserunt repellendus</p>
                </div>
                <div class="row">
                    <div class="col-3"
                    v-for="(element, index) in pricingList"
                    :key="index">
                        <div class="mb-3">
                            <div class="img-wrapper"
                            :v-show="element.img !== undefined">
                                <img
                                :src="`img/${element.img}`" 
                                alt="">
                            </div>
                            <h2>{{element.title}} </h2>
                            <p class="mb-0">{{element.price}} </p>
                        </div>
                        <ul class="me-4 mt-4">
                            <li class="d-flex flex-column justify-content-center align-items-center mb-3"
                            v-for="(element, index) in pricingList[index].list"
                            :key="index">
                                    <p class="mb-2"
                                    v-if="element.item !== 'fas fa-check'">
                                        {{element.item}}
                                    </p>
                                    <i class="mb-3"
                                    v-show="element.item == 'fas fa-check'" 
                                    :class="element.item"></i>
                            </li>
                        </ul>
                        <button class="text-uppercase btn my-btn text-white mt-5"
                        v-show="element.buttonText !== undefined">{{element.buttonText}} </button>
                    </div>
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
    name:'priceList',
    props:['pricingList'],
    data: function(){
        return{
            list:0,
        }
    },
    methods: {
        displayListItems(index){
            if(index > -1){
                this.list = index;
            }
        },
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/styles/partials/_variables.scss";
section{
    position: relative;
}
.img-wrapper{
    height: 100px;
    width:100%;
}
.my-btn {
    background-color: $lightBlueColor;
    padding: 0.5rem 1.5rem;
    border-radius: 0;
    &:hover{
        background-color: $lightBlueColorHover;
    }
}
</style>