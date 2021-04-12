<template>
  <div class="container">
    <quotes-progress-bar :numberOfQuotes="numberOfQuotes()" :maxQuotes="maxQuotes"></quotes-progress-bar>
    <new-quote @quoteAdded="newQuote"></new-quote>
    <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>

    <div class="alert alert-info text-center" role="alert">
      Click a quote to delete it!
    </div>

  </div>
</template>

<script>

import NewQuote from './components/NewQuote.vue';
import QuotesProgressBar from './components/QuotesProgressBar.vue';
import QuoteGrid from './components/QuoteGrid.vue';

export default { 
  data(){
    return{
        quotes:[
          'Test Quote',
        ],
        maxQuotes:10,
    }
  },
  components:{
    'quoteGrid':QuoteGrid,
    'newQuote':NewQuote,
    'quotesProgressBar':QuotesProgressBar,
  },
  methods:{
    newQuote(quote,event){
      if (this.quotes.length < 10) {
        this.quotes.push(quote);
      }
      else{
        event.stopPropagation();   
      }
    },

    deleteQuote(index){
      this.quotes.splice(index,1);
    },

    numberOfQuotes(){
      return this.quotes.length
    }
  }
}
</script>

<style>

</style>
