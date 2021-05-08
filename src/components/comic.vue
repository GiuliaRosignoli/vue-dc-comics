<template>
    <div class="single-image">
       <img v-bind:src="detail.thumb" alt="detail.series">
       <h2>{{ detail.series }}</h2>
    </div>
  
</template>

<script>
export default {
    name: "comic",
    props: ["detail"],

}
</script>

<style lang="scss" scoped>
    .single-image {
       justify-content: center;
       flex-basis: calc(100% / 6 - 20px);
       flex-wrap: wrap;
       padding-bottom: 10px;
       color: #fff;
       img {
           width: 100px;
           height: 100px;
           margin: 20px;
           margin-bottom: 30px;
       }
    }

</style>