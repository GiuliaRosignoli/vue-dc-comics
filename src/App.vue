<template>
  <div id="app">
     <!--Header -->
    <header>
       <Header />
    </header>
    <!--jumbotron -->
    <section>
          <Jumbotron />
    </section>

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
import Jumbotron from '@/components/Jumbotron.vue';
import Products from '@/components/Products.vue';
import Footer from '@/components/Footer.vue';


export default {
    name: 'App',
    components: {
      Header,
      Jumbotron,
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
