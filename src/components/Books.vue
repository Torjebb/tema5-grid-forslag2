<template>
     <div v-for="(book, index) in books" :class="'content__book' + (index)">
      <div><img v-bind:src="'public/images/' + book.cover" class="content__book--img" /></div>
      <h3>{{ book.writers }}</h3>
      <h3 :class="'content__booktitle' + (index)">{{ book.title }}</h3>
   </div>
  
</template>

<script>
export default {
   data () {
      return {

      }
   },
   
   computed: {
      articleOne() {
         return this.$store.getters.getArticleOne;
         
      },

      articleTwo() {
         return this.$store.getters.getArticleTwo;
      },

      articleThree() {
         return this.$store.getters.getArticleThree;
      },

      books() {
         return this.$store.getters.getBooks;
      }
   }
}
</script>

<style>
.content__book--img {
   padding-bottom: 10px;
}

</style>