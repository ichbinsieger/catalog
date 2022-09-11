<template>
  <div>
        <div class="flex items-center justify-between" >
            <h1 class="text-4xl font-semibold tracking-wide">Shirts</h1>
            <p class="text-gray-500 text-xs "> <span> 28 </span>items available </p>
        </div>
        <div class=" px-2 pt-12 grid grid-cols-2 gap-4 md:grid-cols-4 md:gap-4">
            <div  v-for="shirt in shirts" :key="shirt.name">
                <div class="cursor-pointer transition ease-in-out delay-150  hover:-translate-y-1 hover:scale-105  duration-300  w-60">
                    <img class="w-full" :src="shirt.img" alt="">
                    <p class="text-xl pt-2 font-semibold">{{ shirt.name }}</p>
                    <p class="">₦{{shirt.price}} </p>
                </div>
            </div>
        </div>
  </div>
</template>

<script>
import store from '@/store'
    export default {
    data(){
        return{
            shirts: store.state.ShirtStore
        }
    }
}
</script>

<style>

</style>