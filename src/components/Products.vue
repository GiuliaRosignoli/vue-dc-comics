<template>
  <div class="wrapper">
      <div class="grey-bg">
        <div class="container">  Content goes here  </div>
      </div>
       <section class="blue flex">
           <ul class="second-list flex container">
               <li v-for="(item, index) in secondLineLinks" :key="index"><a href="#">{{ item.text }}</a></li>
               <li><a href="#"></a></li>
               <li><a href="#"></a></li>
               <li><a href="#"></a></li>
               <li><a href="#"></a></li>
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
                {text: "DIGITAL COMICS", url: "/digital-comics", current: false},
                {text: "DC MERCHANDISE", url: "/dc-merchandise", current: false},
                {text: "SUBSCRIPTION", url: "/subscription", current: false},
                {text: "COMIC SHOP LOCATOR", url: "/comic-shop-location", current: false},
                {text: "DC POWER VISA", url:"dc-power-visa", current: false},
            ],
        }
    }
}
</script>

<style lang="scss" scoped>

    .grey-bg {
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
        list-style: none;
    }

    .blue.container.flex ul li {
        padding: 1rem;
        font-size: 0.8rem;
        
    }

    .blue.flex .second-list a {
        align-items: center;
        color: #fff;
      }


    
</style>