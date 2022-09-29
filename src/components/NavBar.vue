<template>
    <div class="relative">
        <div class="bg-white fixed top-0 left-0 right-0 py-5 px-10">
        <div class="flex justify-between">
            <h1 class="text-green-500 text-2xl" >Cata<span class="text-blue-300">log</span></h1>
            <div class="flex  space-x-10 ">
                <div class="relative  ">
                        <transition class="p-2" name="fade">
                            <input v-if="showsearchbar" type="text" placeholder="search" class=" w-60 rounded-md border border-gradient-to-r from-green-500 to-blue-500 outline-none" >
                        </transition>
                        <span @click="OpenSearch" class="bottom-1 cursor-pointer right-2 absolute p-1 rounded-sm flex items-center justify-center "><i class="ri-search-2-line text-xl  text-transparent bg-clip-text bg-gradient-to-br from-green-500 to-blue-500 "></i> </span>
                </div>
                <div @click="openCart">
                    <p class="flex items-center"><i class="ri-shopping-cart-line text-2xl"></i> <sup>(0)</sup></p>
                </div>
            </div>
        </div>
        </div>

        <!-- categories -->
        <div class="pt-20">
              <div class="border-y flex items-center py-5 justify-center">
                    <div class="flex w-full justify-center space-x-20 overflow-x-auto whitespace-nowrap ">
                            <div class="     " v-for="category in categories" :key="category" >   
                                <p class=" transition ease-in-out delay-150 hover:-translate-y-1 hover:scale-110  duration-300 cursor-pointer hover:border-b-2 pb-2  hover:border-green-500 " > {{ category }} </p>
                                
                            </div>
                    </div>
              </div>
        </div>
         <!-- cartItems  -->
         <div class="fixed w-full top-0 right-0 left-0 bg-slate-400 bg-opacity-30 h-screen ">
            <div class="z-20 w-full flex justify-center items-center mt-20 ">
                <cartItems class="   " />
            </div>
         </div>
    </div>
</template>

<script>
import store from '@/store'
import CartItems from './CartItems.vue';
    
export default {
    data() {
        return {
            categories: store.state.categories,
            showsearchbar: false
        };
    },
    methods: {
        OpenSearch() {
            this.showsearchbar = !this.showsearchbar;
        }
    },
    components: { CartItems }
}
</script>

<style>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.25s ease-out;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>