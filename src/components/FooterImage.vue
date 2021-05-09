<template>
  <img v-bind:src="image" alt="">
</template>

<script>

export default {
    name: "FooterImage.vue",
    data(){
        return {
            image: "../assets/img/dc-logo-bg.png",
        }
    }

}


</script>

<style lang="scss" scoped>
@import "../styles/general.scss"; 
@import "../styles/vars.scss";
@import "../styles/utilities.scss";

img {
    width: 30rem;
    padding: 15px;
}

</style>