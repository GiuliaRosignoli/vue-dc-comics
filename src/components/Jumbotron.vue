<template>
    <img class="jumbotron" v-bind:src="image" alt="">
</template>

<script>
export default {
    name: "Jumbotron",
    data(){
        return {
              image: "../assets/img/jumbotron.jpg",
        }
    }
}
</script>

<style lang="scss" scoped>

    .jumbotron {
        width: 100%;
        height: 30rem;
        object-fit: cover;
        object-position: top;
    }
    
</style>