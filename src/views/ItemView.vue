<template>
  <div>
      <div>
        <NavBar/>
      </div>
      <div>
        <ItemPage/>
      </div>

  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue';
import ItemPage from '@/components/ItemPage.vue';
export default {
    components: { NavBar, ItemPage }
}
</script>

<style>

</style>