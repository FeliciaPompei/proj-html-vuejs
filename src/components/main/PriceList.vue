<template>
    <section class="container text-center">
        <div class="row">
            <div class="col-12">
                <h1>Pricing Plans</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam magnam molestiae architecto eligendi earum, deserunt repellendus</p>
            </div>
            <div class="row">
                <!-- V-for -->
                <div class="col-3 d-flex">
                    <ul 
                    v-for="(element, index) in pricingList"
                    :key="index">
                        <li d-flex flex-column>
                            {{element.type}}
                            {{element. price}}
                            {{element. numberOfCourses}}
                            {{element. days}}
                            <div :class="(element == 'check') ? 'check' : 'cross'">
                            </div>
                            <button class="btn btn-info">{{element. button}}</button>
                        </li>
                    </ul>
                </div>
                <div class="col-3">
                    <!-- <ul>
                        <li
                        v-for="(element, index) in pricingList"
                        :key="index">
                            {{element}}
                        </li>
                    </ul> -->
                </div>

            </div>
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
.check:before{
    content: '\2713';
}
</style>