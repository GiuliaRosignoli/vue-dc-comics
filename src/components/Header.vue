<template>
  <header class="flex container">
    <a href="#">
        <img v-bind:src="logo" alt="logo">
    </a>
    <div class="filler"></div>
    <nav class="flex">
        <ul class="first-list flex">
            <li  v-for="(link, index) in links" v-bind:key="index"><a href="#">{{ link.text }}</a></li>
        </ul>
  </nav>
  </header>
 
</template>

<script>        /* SCRIPT STARTS HERE */
export default {
    name: 'Header',
    data(){
        return {
            links: [
                {text: "CHARACTERS", url: "/characters", current: false },
                {text: "COMICS", url: "/comics", current: true},
                {text: "MOVIES", url: "/movies", current: false},
                {text: "TV", url: "/tv", current: false},
                {text: "GAMES", url: "/games", current: false},
                {text: "COLLECTIBLES", url: "/", current: false},
                {text: "VIDEO", url: "/video", current: false},
                {text: "FANS", url: "/fans", current: false},
                {text: "NEWS", url: "/news", current: false},
                {text: "SHOP", url: "/shop", current: false},
            ],
             logo: "../assets/img/dc-logo.png",
          
        }
    }
}
</script>

<style lang="scss" scoped> /* STYLE STARTS HERE */
@import "../styles/general.scss"; 
@import "../styles/vars.scss";
@import "../styles/utilities.scss";


 header {
     padding: 2rem;
     text-align: center;
 }

 .container a img {
    width: 5rem;
}

.first-list {
    justify-content: flex-end;
    align-items: center;
}

.first-list li a {
    justify-items: end;
    color: rgb(66, 65, 65);
}

.filler {
    flex-grow: 1;
}



</style>