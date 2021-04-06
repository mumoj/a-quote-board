<template>
  <div class="container">
    <new-quote @quoteAdded ="newQuote"></new-quote>
    <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';

export default {
  data(){
    return{
        quotes:[
          'Test Quote',
        ],
        maxQuotes:10
    }
  },
  components:{
    'quoteGrid':QuoteGrid,
    'newQuote':NewQuote,
  },
  methods:{
    newQuote(quote){
      this.quotes.push(quote);
    },
    deleteQuote(index){
      this.quotes.splice(index,1);
    },
    
  }

  
}
</script>

<style>

</style>
