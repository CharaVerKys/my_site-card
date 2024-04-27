<template>
<grid></grid>
<diagRD></diagRD>
</template>

<script>
import diagRD from './diagonalRootDiv';
import grid from './grid';


export default{
    components:{
        diagRD,
        grid
    }
}
</script>

<style>
* {
    margin: 0;
    height: 100%;
    width: 100%;
}

body{
    overflow: hidden;
    background-color: slategrey;
    opacity: 0.7;
}
</style>