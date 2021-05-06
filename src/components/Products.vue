<template>
  <div class="wrapper">
      <div class="grey-bg">
        <div class="container temporary"> -->  Content goes here  </div>
      </div>
       <section class="blue flex">
           <ul class="second-list flex container">
               <li v-for="(item, index) in secondLineLinks" :key="index"><a class="flex" href="#"> <img v-bind:src="item.image" alt="icons"> {{ item.text }}</a></li>
               <li ><a class="flex" href="#"></a></li>
               <li class="flex"><a href="#"></a></li>
               <li class="flex"><a href="#"></a></li>
               <li class="flex"><a href="#"></a></li>
           </ul>
       </section>
  </div>
 
</template>

<script>
export default {
    name: 'Products',
    data(){
        return {
            secondLineLinks: [
                {text: "DIGITAL COMICS", image: "../assets/img/buy-comics-digital-comics.png",  url: "/digital-comics", current: false},
                {text: "DC MERCHANDISE", image: "../assets/img/buy-comics-merchandise.png", url: "/dc-merchandise", current: false},
                {text: "SUBSCRIPTION", image: "../assets/img/buy-comics-subscriptions.png", url: "/subscription", current: false},
                {text: "COMIC SHOP LOCATOR", image: "../assets/img/buy-comics-shop-locator.png", url: "/comic-shop-location", current: false},
                {text: "DC POWER VISA", image: "../assets/img/buy-dc-power-visa.svg", url:"dc-power-visa", current: false},
            ],
            
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../styles/general.scss"; 
@import "../styles/vars.scss";
@import "../styles/utilities.scss";

    .temporary{             /* Temporay class */
        color: $primary; 
        font-size: 2rem;
        text-align: center;
    }

    .grey-bg {         /* Pictures section to be created here */
        height: 100px;
        background-color: rgb(31, 30, 30);
    }

    .blue {
        height: 120px;
        max-height: 100%;
        background-color: rgb(38, 125, 211);
    }

    .second-list { /*Second list */
        justify-content: center;
        align-items: center;
        display: flex;
    }


    .second-list li {
        align-items: center;
        a {
            color: $primary;
        align-items: center;
        }
        a img {
            width: 3rem;
        padding: 0.5rem;
        }
    }


    
</style>