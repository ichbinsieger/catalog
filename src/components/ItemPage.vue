<template>
  <div>
     <div class="w-full pt-10 flex flex-col items-center justify-center" >
            <div class=" w-full flex justify-between px-20">
                <span> <i class="ri-arrow-left-line text-2xl"></i> </span>
                <i class="ri-heart-line text-2xl"></i> 
             </div>
           <div class= " rounded-md h-2/6 p-10 flex flex-col items-center justify-center w-2/4 bg-gradient-to-r from-green-300 to-blue-400">  <img class="w-full h-full " :src="item.img" alt="" srcset=""> </div>
     </div>
  </div>
</template>

<script>
import store from '@/store'
    
export default {
    data(){
        return{
            item: store.state.ShirtStore[0]
        }
    }
}
</script>

<style>

</style>