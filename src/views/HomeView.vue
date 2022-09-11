<template>
  <div class="home bg-white">
      <div>
        <NavBar/>
      </div>
      <div class="px-10 py-5">
        <ShirtShop/>
      </div>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue';
import ShirtShop from '@/components/shop/ShirtShop.vue';
// @ is an alias to /src


export default {
  name: 'HomeView',
  components: {
    NavBar,
    ShirtShop
}
}
</script>
