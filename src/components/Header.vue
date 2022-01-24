<template>
  <div v-for="page in navigationPages">{{ page.title }}</div>
</template>

<script>
export default {
   data () {
      return {

      }
   },
   
   computed: {
      navigationPages() {
         return this.$store.getters.getNavigation;
      }
   }
}
</script>

<style>

</style>