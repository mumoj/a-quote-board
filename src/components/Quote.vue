<template>
    <div class="quote col-sm-6 col-md-4 col-lg-3">
        <div class="card.card-default">
            <div class="card-body">
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
    .card-body{
        font-family:cursive;
        font-size: 24px;
        color:grey;
    }
    .quote{
        cursor:pointer;

    }
    .quote:hover{
        background:#ffe2e2;
    }
    
</style>