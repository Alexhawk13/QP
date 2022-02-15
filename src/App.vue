<template>
  <div class = "wrapper">
    <Header></Header>
    <Banner></Banner>
    <GetStarted></GetStarted>
    <Comments></Comments>
    <FAQ></FAQ>
    <Contact></Contact>
    <Footer></Footer>
  </div>
  
</template>

<script>
import Header from "./components/Header.vue";
import Banner from "./components/Banner.vue";
import GetStarted from "./components/GetStarted.vue";
import Comments from "./components/Comments.vue";
import FAQ from "./components/FAQ.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue"

export default {
  name: "App",
  components: {
    Header,
    Banner,
    GetStarted,
    Comments,
    FAQ,
    Contact,
    Footer
  },
};
</script>

<style>
@import url("//db.onlinewebfonts.com/c/a294fb387eda4c52a3224aa008dcb2fe?family=Museo+Sans+Cyrl+500+700");
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
#app {
  font-family: 'Montserrat', sans-serif;
}
:root {
  --main-color: #333;
  --secondary-color: #4F4F4F;
}
h1,h2,h3,h4,button,.logo {
  font-family: 'Museo Sans', sans-serif ;
  margin: 0
}

h2 {
  font-weight: 500;
  font-size: 40px;
  line-height: 115%;
}

body {
  overflow-x: hidden;
  margin: 0;
  color: var(--main-color)
}

.logo {
  font-weight: bold;
  font-size: 15px;
  line-height: 16px;
}

.container {
  padding-left: 20px;
  padding-right: 20px;
}

.button {
  border-width: 1px;
}

.button:hover {
  background-color: #7181FC;
  cursor: pointer;
}

.button:active {
  background-color: #354BF4;
}

.disabled {
  background-color: #E0E0E0;
}

mark{
  background-color: rgba(98,72,255,0.1);
}


@media screen and (min-width: 768px) {
  h1 {
    font-size: 64px;
    line-height: 110%;
    font-weight: 500;
  }

  h2 {
    font-size: 56px;
  }
  
  .container {
    padding-left: 40px;
    padding-right: 40px;
  }
}

@media screen and (min-width: 1440px) {
  .container{
    padding-left: 120px;
    padding-right: 120px;
  }
}
</style>
