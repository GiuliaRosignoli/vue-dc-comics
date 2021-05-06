<template>
  <footer> 
    <div class="container">
        <div class="footer-wrapper flex">
          <div class="footer-wrapper-col">
            <ul>
              <li>DC COMICS</li>
              <li>Characters</li>
              <li>Comics</li>
              <li>Movies</li>
              <li>TV</li>
              <li>Games</li>
              <li>Videos</li>
              <li>News</li>
            </ul>
            <ul>
              <li>SHOP</li>
            </ul>
          </div>
        </div>
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

    .footer-wrapper-col {
      flex-direction: column;
    }

    .footer-wrapper-col ul li {
      color: $primary;
    }

</style>