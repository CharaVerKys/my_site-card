<template>
    <div class="container">
        <img class="car" src="../../assets/mj_car.png" @click="link_playlist">
  </div>

</template>

<style lang="scss" scoped>
.container {


    .car {
        opacity: 0.83;
        margin-left: -10%;
        margin-top: 5%;
        cursor: pointer;
        width: 100%;
        height: fit-content;
        transform: rotate3d(1, 0.5, 0.5, 7deg);

        @media screen and (max-width: 1250px) {
            margin-top: 22%;
            width: 110%;
            margin-left: -20%;
        }
    }



}
</style>

<script>

export default {
   
    methods: {
        link_playlist() {
            window.location.href = "https://www.youtube.com/playlist?list=PLybBpPCOgFt6_nW9iddytS3hQqj7ZvDvA";
        }
    }    
}

</script>