<template>
  <footer> 
    <div class="first-container">  <!--Genral container - root -->
        <div class="second-container">  <!--Inner container - width 1200px -->
          <div class="footer-wrapper container flex">
            <div class="footer-wrapper-col">
              <ul>
                <li v-for="(items, ind) in linkList" v-bind:key="ind"><a href="#">{{ items.text }}</a></li>
              </ul>
              <ul>
                <li v-for="(list, i) in secondLinkList" v-bind:key="i"><a href="#">{{ list.text }}</a></li>
              </ul>
            </div>
            <ul>
              <li v-for="(list, i) in thirdLinkList" v-bind:key="i"><a href="#">{{ list.text }}</a></li>
            </ul>
            <div class="filler"></div>
            <div class="image-cont flex"> 
              <FooterImage />
            </div>
        </div>
        <div class="last-section">
            <!-- Button and social media icons -->
        </div>
        
        </div> <!--Inner container -->
        
    </div>  <!--First container - general -->
  </footer>
</template>


<script>

import FooterImage from "@/components/FooterImage.vue";

export default {
    name: 'Footer',
     components: {
        FooterImage,
    },
    data() {
      return {
        linkList: [
                {text: "DC COMICS", url: "/list"},
                {text: "Characters", url: "/characters"},
                {text: "Comics", url: "/comics"},
                {text: "Movies", url: "/movies"},
                {text: "TV", url: "/tv"},
                {text: "Games", url: "/games"},
                {text: "Video", url: "/video"},
                {text: "News", url: "/news"},
  
            ],
          secondLinkList: [
                {text: "SHOP", url: "/shop"},
                {text: "Shop DC", url: "/shop-dc"},
                {text: "Shop DC collectibles", url:"/shop-dc-collectibles"},
                {text: "Movies", url: "/movies"},
                {text: "TV", url: "/tv"},
                {text: "Games", url: "/games"},
                {text: "Video", url: "/video"},
                {text: "News", url: "/news"},
          ],
          thirdLinkList: [
              {text: "DC", url: "/dc"},
                {text: "Terms of Use", url: "/terms-of-use"},
                {text: "Privacy policy (New)", url:"/privacy-policy"},
                {text: "AD Choices", url: "/ad-choices"},
                {text: "Advertising", url: "/advertsing"},
                {text: "Jobs", url: "/jobs"},
                {text: "Subscriptions", url: "/subscriptions"},
                {text: "Talent Workshops", url: "/talent-workshops"},
          ],
      }
    }
}

</script>
 
<style lang="scss" scoped>   /* STYLE */
@import "../styles/general.scss"; 
@import "../styles/vars.scss";
@import "../styles/utilities.scss";


    footer {
      height: 430px;
      background-image: url("../assets/img/footer-bg.jpg"); 
    }
   
    .footer-wrapper-col {
      flex-direction: column;
    }

    ul {
        margin-top: 30px;
        padding: 10px;
        li {
          padding: 3px;
        a {
          font-size: 0.8rem;
          color: $primary;
        }
      }
    }
      
    .last-section {
      width: 100%;
      height: 6rem;
      background-color: $grey;
    }

    .filler {
      flex-grow: 1;
    }

</style>