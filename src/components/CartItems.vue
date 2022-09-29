<template>
    <div class=" p-5 w-2/4 relative bg-white ">
        <div class=" flex border-b border-gray-200 w-full">
            <h1 class="text-xl font-semibold">Cart</h1>
        </div>
        <div class="flex">
            <div class=" p-2 border-b">
                    <img class="w-40" :src="item.img" alt="">
            </div>
            <div>
                <p class="flex flex-wrap font-semibold tracking-wide whitespace-pre-wrap text-xl "> {{ item.name }} </p>
                 <div class=" flex space-x-2 pt-2  items-center ">
                    <p @click="decreaseUnit" class="px-1 cursor-pointer font-semibold text-2xl"> - </p>
                    <div class="border-2  border-gray-700 mt-1  h-5 w-5 flex items-center justify-center  "> <p class="text-sm p-1" > {{ unit }}  </p>  </div>
                    <p @click="increaseUnit" class=" cursor-pointer px-1 font-semibold text-2xl"> + </p>
                 </div>
            </div>
        </div>
    </div>
</template>

<script>
    import store from '@/store';
export default {
    data(){
        return{
            item: store.state.ShirtStore[0],
            unit:1,
        }
    },
    methods:{
        increaseUnit(){
            this.unit++
        },
        decreaseUnit(){
            if (this.unit >1) {
                this.unit--
            }
            else this.unit == 1
        }
    }
}
</script>

<style>

</style>