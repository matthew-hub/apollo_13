<template>
  <div id="app">
    <div id="wrapper">
      <Header />
      <Main v-bind:phases="phasesData" v-bind:facts="factsData" />
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from "./components/layout/Header.vue";
import Main from "./components/layout/Main.vue";
import Footer from "./components/layout/Footer.vue";
import phasesData from "./data/phase.json";
import factsData from "./data/facts.json";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer
  },
  data() {
    return {
      phasesData: phasesData.phases,
      factsData: factsData.facts
    };
  },
  mounted() {
    console.log(phasesData);
    console.log(factsData);
  }
};
</script>

<style lang="scss">
@import "./assets/styles/reset.css";

@font-face {
  font-family: Anton;
  src: url("assets/font/Anton-Regular.ttf");
}

@font-face {
  font-family: Ultra;
  src: url("assets/font/Ultra-Regular.ttf");
}

@font-face {
  font-family: OpenSans;
  src: url("assets/font/OpenSans-SemiBold.ttf");
}
@font-face {
  font-family: BlackHanSans;
  src: url("assets/font/BlackHanSans-Regular.ttf");
}

html,
body {
  width: 100%;
  height: 100%;
}

html {
  font-size: 62.5%;
}

#app {
  font-family: OpenSans;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  min-height: 100%;
  background-color: #f7f7f7;
}

#wrapper {
  padding: 25px 20px;
  width: 100%;
  min-width: 375px;
  min-height: 100%;
  display: grid;
  grid-template-columns: 335px;
  grid-template-rows: auto;
  grid-row-gap: 50px;
  justify-self: center;
  justify-content: center;

  @media (min-width: 940px) {
    grid-template-columns: 900px;
  }
}
</style>
