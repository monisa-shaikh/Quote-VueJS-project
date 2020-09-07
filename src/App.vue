<template>
    <div class="container">
      <app-header :quotesCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
      <app-new-quotes @quoteAdded="newQuote"></app-new-quotes>
      <app-quote-grid :quotes="quotes" @quoteDelete="deleteQuote"> </app-quote-grid>
      <div class="row">
        <div class="col-sm-12 text-center">
          <div class="alert alert-info">Info:click on quote to delete !!</div>
        </div>
      </div>
    </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import newQuotes from './components/newQuotes.vue';
import header from './components/header.vue';


    export default {
        data:function () {
          return{
            quotes:['sample quotes'],
            maxQuotes:10
          }
          
        },
        methods:{
          newQuote(quote){
            if(this.quotes.length>=this.maxQuotes){
              return alert("plz delete quotes first!!!");
            }
             this.quotes.push(quote);
          },
          deleteQuote(index){
            this.quotes.splice(index,1);
          }
        },
        components:{
          appQuoteGrid:QuoteGrid,
          appNewQuotes:newQuotes,
          appHeader:header
        }
    }
</script>

<style>
</style>
