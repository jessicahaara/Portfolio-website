<template>
  <div id="app">
    <Header @scrollclick="scroll" v-if="showHeader" class="fixed" />
    <MainFirst @scrollclick="scroll" />
    <About id="about" />
    <Lia id="lia" />
    <Projects id="projects" />
    <Contact id="contact" />
  </div>
</template>

<script>
import Header from "./components/header/Header.vue";
import MainFirst from "./components/main/MainFirst.vue";
import About from "./components/main/About.vue";
import Contact from "./components/main/Contact.vue";
import Projects from "./components/main/Projects.vue";
import Lia from "./components/main/Lia.vue";

export default {
  name: "App",
  components: {
    Header,
    MainFirst,
    About,
    Lia,
    Projects,
    Contact,
  },

  created() {
    window.addEventListener("scroll", this.handleScroll);
  },

  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },

  data() {
    return {
      showHeader: true,
      scrollPosition: 0,
    };
  },

  methods: {
    scroll(id) {
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
      });
    },

    handleScroll() {
      if (this.scrollPosition < window.scrollY) {
        this.showHeader = false;
      }

      if (this.scrollPosition > window.scrollY) {
        this.showHeader = true;
      }
      this.scrollPosition = window.scrollY;
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Assistant:wght@300;500&family=Raleway:wght@400;700&display=swap");

:root {
  box-sizing: border-box;
  margin: 0px;
  padding: 0px;
  --beige: #f6e5dc;
  --dark-beige: #caa38e;
  --light-green: #cedccf;
  --green: #93b396;
  --almost-black: #444440;
  --purple: #b393b0;
}

html,
body {
  background-color: var(--beige);
}

.fixed {
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  background-color: var(--beige);
  z-index: 1;
}
</style>
