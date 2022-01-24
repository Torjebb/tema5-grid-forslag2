<template>
  <div>{{ information.address }}</div>
</template>

<script>
export default {
   data () {
      return {

      }
   },
   computed: {
      information () {
         return this.$store.getters.getAddress
      }
   }  
}
</script>

<style>

</style>