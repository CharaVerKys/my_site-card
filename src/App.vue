<template>
    <diagND></diagND>
    <grid></grid>
    <diagBD></diagBD>
</template>

<script>
import diagBD from './diag/diagonalBigDiv';
import diagND from './diag/diagonalNamedDiv';
import grid from './grid';


export default{
    components:{
        diagND,
        diagBD,
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
    /* background-color: rgb(147, 96, 177); */
    background: linear-gradient(to right,#6a9cff, #84049e);
    opacity: 0.7;
}
</style>