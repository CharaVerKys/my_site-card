<template>
    <div class="root">


    </div>
</template>

<style lang="scss" scoped>
@import './variables.scss';
//dev , testing
.root {
    width: 400px;
    height: 400px;
    border-radius: 50%;
top:17%;
left:10%;
position: relative;
    @if $debug {
        border: red 1px solid;
    }    
}

@media screen and (min-width: 800px) and (max-width: 949px){
    .root{
        left:3%;
    }
}

@media (max-width: 799px) {
    .root{
        display:none;
    }
} //для будующей адаптации под телефоны
</style>