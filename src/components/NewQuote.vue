<template>
    <div class="row justify-content-center">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 col-lg-5 form-group">
                <label>Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>

            <div class="form-group">
                <button class="btn btn-outline-success" @click.prevent="createNew"> New Quote </button>
            </div>
        </form>
        
    </div>
</template>

<script>
export default {
    data:function(){
        return{
            'quote':''
        };
    },
    methods:{
        createNew(){
           this.$emit('quoteAdded', this.quote);
           this.quote = '';


        },
    }
    
} 
</script>

<style>
    
</style>>