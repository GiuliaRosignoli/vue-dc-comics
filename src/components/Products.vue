<template>
  <div class="wrapper">
     
            <div class="grey-bg">
                <div class="comics container flex"> 
                    <comic v-for="(comic, index) in items" :key="index" :detail="comic"  />
                </div>
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
import comic from "@/components/comic.vue";

export default {
    name: 'Products',
    components: {
        comic,
    },
    data(){
        return {
            items: [
                        {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX',
                price: '$19.99',
                series: 'Action Comics',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01',
                price: '$3.99',
                series: 'American Vampire 1976',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb',
                price: '$16.99',
                series: 'Aquaman',
                type: 'graphic novel',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76',
                price: '$2.99',
                series: 'Batgirl',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
                price: '$3.99',
                series: 'Batman',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
                price: '$2.99',
                series: 'Batman Beyond',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8',
                price: '$3.99',
                series: 'Batman/Superman',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk',
                price: '$4.99',
                series: 'Batman/Superman Annual',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8',
                price: '$5.99',
                series: 'Batman: The Joker War Zone',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY',
                price: '$6.99',
                series: 'Batman: Three Jokers',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX',
                price: '$4.99',
                series: 'Batman: White Knight Presents: Harley Quinn',
                type: 'comic book',
            },
            {
                thumb:
                    'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq',
                price: '$16.99',
                series: 'Catwoman',
                type: 'graphic novel',
            },
        ],

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



    .grey-bg {         /* Pictures section to be created here */
        width: 100%;
        align-items: center;
        flex-wrap: wrap;
        background-color: rgb(31, 30, 30);
    }

    /* Container */
    .comics.container {
        justify-content: center;
        flex-wrap: wrap;
        width: 70%;
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