<template>
    <div class="card col-sm-6 col-md-4 col-lg-3 m-3">
            <div class="card-body">
                <div class="card-text">
                    <slot></slot>
                </div>
            </div>
    </div>
</template>

<script>
export default {

    
}
</script>

<style>
    .card-text{
        font-family:cursive;
        font-size: 16px;
        color:grey;
    }
    .card-header{
        cursor:pointer;
        border-style:dashed;
        border-width:1px;
        border-color:rgb(15, 146, 233);
        border-radius:5px;
    }
    .card:hover{
        background:#ffe2e2;
        border-style:none;
        
    }
    
</style>