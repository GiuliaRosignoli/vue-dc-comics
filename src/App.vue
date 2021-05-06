<template>
  <div id="app">
     <!--Header -->
    <header>
       <Header />
    </header>
  

  <!--Main -->
   <main>
     <Products />
   </main>

  <!--Footer -->
   <footer>

     <Footer />
   </footer>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Products from '@/components/Products.vue';
import Footer from '@/components/Footer.vue';


export default {
    name: 'App',
    components: {
      Header,
      Products,
      Footer,
    }
};
</script>

<style lang="scss">
@import "./styles/general.scss";
@import  "./styles/utilities.scss";
@import "./styles/vars.scss";

</style>
