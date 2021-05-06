<template>
  <footer> 
    <div class="container">
        <div>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptates pariatur itaque repellat nemo earum recusandae voluptas harum! Corrupti voluptatum dolores cupiditate! Tempore officia possimus consequatur amet quos laudantium atque quibusdam!</div>
    </div>
  </footer>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style lang="scss" scoped>
@import "../styles/general.scss"; 
@import "../styles/vars.scss";
@import "../styles/utilities.scss";


    footer {
      height: 320px;
       background-image: url("../assets/img/footer-bg.jpg"); 
    }
</style>