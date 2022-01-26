<template>

<div class="content">
<div class="section__header">Latest</div>
	<Homepage />
<div class="section__header">Books</div>
	<Books />
<div class="section__header">Journal</div>
    <Subscribe />
</div>


<!-- 
<div class="content">
    <div class="content__mainart">Main art</div>
    <div class="content__secart">Sec art</div>
    <div class="content__thirdart">Third art</div>
    <div class="content__book1 book">Book 1</div>
    <div class="content__book2 book">Book 2</div>
    <div class="content__book3 book">Book 3</div>
    <div class="content__book4 book">Book 4</div>
    <div class="content__book5 book">Book 5</div>
    <div class="content__book6 book">Book 6</div>
</div>

   -->
</template>

<script>
import Header from '../components/Header.vue'
import Homepage from '../components/Homepage.vue'
import Footer from '../components/Footer.vue'
import Books from '../components/Books.vue'
import Subscribe from '../components/Subscribe.vue'

export default {
	components: {
		Header,
		Homepage,
		Footer,
		Books,
        Subscribe
	}
}
</script>

<style>


* {
	box-sizing: border-box;
	margin: 0;
	padding: 0;
	
}

						/* GRID */
 .content {
    display: grid;
    margin: 0 auto;
    grid-template-columns: repeat(6, 1fr);
    grid-gap: 0 12px;
    width: 100%;
	padding: 0 23px;
    
}

.section__header {
	font-family: 'JetBrains Mono';
  	font-style: normal;
  	font-weight: normal;
	font-size: 30px;
   	line-height: 40px;
	text-align: center;
	grid-column: 1 / 7;
	padding-bottom: 40px;
	padding-top: 100px;
}

.content__mainart {
    grid-column: 2 / 6;
}

.content__secart {
    grid-column: 1 / 4;  
}

.content__thirdart {
    grid-column: 4 / 7;
}

.content__book0 {
    grid-column: 1 / 2;
}
.content__book1 {
    grid-column: 2 / 3;
}
.content__book2 {
    grid-column: 3 / 4;
}
.content__book3 {
    grid-column: 4 / 5;
}
.content__book4 {
    grid-column: 5 / 6;
}
.content__book5 {
    grid-column: 6 / 7;
}


/* Responsive layout - makes the three columns stack on top of each other instead of next to each other */
@media screen and (max-width: 900px) {
  .content__secart,
  .content__thirdart,
  .content__mainart {
    grid-column: 1 / 7;
  }
  .content__book0 {
      grid-column: 1 / 3;
  }
  .content__book1 {
      grid-column: 3 / 5;
  }
  .content__book2 {
      grid-column: 5 / 7;
  }
  .content__book3 {
      grid-column: 1 / 3;
  }
  .content__book4 {
      grid-column: 3 / 5;
  }
  .content__book5 {
      grid-column: 5 / 7;
  }
}


</style>