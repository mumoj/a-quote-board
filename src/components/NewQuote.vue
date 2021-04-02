<template>
    <div class="row justify-content-center">

    <div class="col-6 text-center">
        <form>
            <div class="form-group">
                <label class="text-muted">Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>
            <button class="btn btn-outline-dark" @click.prevent="createNew"> New Quote </button>
        </form>
    </div>

        
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

<style scoped>
    label{
            font-size: 30px;
    }
    

</style>
    
