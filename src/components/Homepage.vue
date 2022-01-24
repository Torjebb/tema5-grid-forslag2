<template>
<div class="content__mainart">
   <div class="content__mainart--text">
  <h2>{{  articleOne.title }}</h2>
  <h3 class="content__mainart--ingress">{{ articleOne.lead }}</h3>
   </div>
  <img class="content__mainart--img" v-bind:src="'/images/' + articleOne.preview.image" /> 
</div>

<div class="content__secart">
   <div class="content__secart--text">
   <h2>{{  articleTwo.title }}</h2>
  <h3 class="content__thirdart--ingress">{{ articleTwo.lead }}</h3>
   </div>
  <img v-bind:src="'/images/' + articleTwo.preview.image" /> 
</div>  

<div class="content__thirdart">
   <div class="content__thirdart--text">
   <h2>{{  articleThree.title }}</h2>
  <h3 class="content__thirdart--ingress">{{ articleThree.lead }}</h3>
   </div>
  <img v-bind:src="'/images/' + articleThree.preview.image" />
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
   }
}

</script>

<style>
h2 {
   font-family: 'JetBrains Mono';
   font-style: normal;
   font-weight: 400;
   font-size: 50px;
   line-height: 66px;
   text-align: center;
   padding-bottom: 20px;
}

h3 {
   font-family: 'JetBrains Mono';
   font-style: normal;
   font-weight: normal;
   font-size: 20px;
   line-height: 26px;
}

.content__mainart {
   margin-bottom: 100px;
}

.content__mainart--ingress,
.content__secart--ingress,
.content__thirdart--ingress {
   text-align: center;
}

.content__mainart--text {
   padding: 0 15%;
   margin: 0 auto;
}

.content__secart--text,
.content__thirdart--text {
   padding: 0 15%;
}

/* Fjern padding på mobil */
@media screen and (max-width: 900px) {
   .content__mainart--text,
   .content__secart--text,
   .content__thirdart--text {
      padding: 0 0;
   }
} 



</style>