<template>
    <div class="external">
        <div class="container">

            <iframe width="560" height="315" src="https://www.youtube.com/embed/nCQ_zZIiGLA?si=bsScv_OadcavElCS&amp;controls=0&amp;autoplay=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


        </div>
    </div>

</template>
<style lang="scss" scoped>
.external {
    display: flex;
    align-items: end;
    margin: 10% 0 0 15%;
}

.container {
    transform: rotate(-15deg);
@media screen and (max-width: 1150px) {
 height: 165px;   
}
@media screen and (min-width: 1400px) {
 height: 130%;   
 transform: rotate(-5deg);
}

}

</style>