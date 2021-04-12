<template>
    <div class="progress-bar-striped bg-info text-center w-10 mt-3" role="progressbar" 
    :style="{width:numberOfQuotes/maxQuotes * 100 + '%'}">
        {{numberOfQuotes}} / {{maxQuotes}}
    </div>
</template>

<script>
export default {
    props:['numberOfQuotes', 'maxQuotes' ],
}
</script>

<style>
    
</style>