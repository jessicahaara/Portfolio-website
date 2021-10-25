<template>
  <nav class="nav">
    <ul class="desktop">
      <li class="normal first" @click="scroll('about')">
        <span>1.</span> Om mig
      </li>
      <!-- <li class="normal second" @click="scroll('lia')">
        <span>2.</span> LIA 2022
      </li> -->
      <li class="normal third" @click="scroll('projects')">
        <span>2.</span> Projekt
      </li>
      <li class="normal fourth" @click="scroll('contact')">
        <span>3.</span> Kontakt
      </li>
      <li class="last">
        <SmallButton v-bind:buttonTitle="'CV'" @click.native="openResume()" />
      </li>
    </ul>

    <img
      src="@/assets/burger-menu.png"
      alt="nav menu"
      class="mobile"
      @click="showNav = true"
    />

    <div class="mobile-nav" v-if="showNav">
      <div class="top">
        <h1 @click="showNav = false">JH</h1>
        <p @click="showNav = false">X</p>
      </div>
      <ul @click="showNav = false">
        <li class="normal first" @click="scroll('about')">
          <span>1.</span> Om mig
        </li>
        <!-- <li class="normal second" @click="scroll('lia')">
          <span>2.</span> Lia 2022
        </li> -->
        <li class="normal third" @click="scroll('projects')">
          <span>2.</span> Projekt
        </li>
        <li class="normal fourth" @click="scroll('contact')">
          <span>3.</span> Kontakt
        </li>
        <li class="last">
          <SmallButton v-bind:buttonTitle="'CV'" @click.native="openResume()" />
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
import SmallButton from "../buttons/SmallButton.vue";
export default {
  components: {
    SmallButton,
  },

  data() {
    return {
      showNav: false,
    };
  },

  methods: {
    openResume() {
      window.open("/JessicaHaaraCV.pdf", "_blank");
    },
    scroll(id) {
      this.$emit("scrollclick", id);
    },
  },
};
</script>

<style scoped>
ul {
  font-family: "Assistant", sans-serif;
  text-transform: uppercase;
  font-weight: bold;
  color: var(--almost-black);
  display: flex;
  align-items: center;
}

.desktop li {
  cursor: pointer;
  margin-left: 50px;
  transition: 0.2s;
}

li {
  list-style-type: none;
}

li span {
  color: var(--green);
}

.normal:hover {
  color: var(--green);
  margin-top: -5px;
}

.first {
  animation: nav-animation 0.1s;
}

.second {
  animation: nav-animation 0.2s;
}

.third {
  animation: nav-animation 0.3s;
}

.fourth {
  animation: nav-animation 0.4s;
}

.last {
  animation: nav-animation 0.5s;
}

.mobile {
  display: none;
}

@keyframes nav-animation {
  0% {
    margin-top: -60px;
    margin-right: 40px;
    opacity: 0;
  }

  100% {
    margin-top: 0;
    opacity: 1;
    margin-right: 0;
  }
}

@media only screen and (max-width: 852px) {
  .desktop {
    display: none;
  }

  .mobile {
    display: inline-block;
    width: 40px;
    height: 40px;
    animation: nav-animation 0.2s;
    margin: 0;
  }

  .mobile-nav {
    width: 100vw;
    height: 100vh;
    background-color: var(--almost-black);
    position: fixed;
    top: 0;
    left: 0;
    z-index: 1;
  }

  .mobile-nav .top {
    width: 90%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .mobile-nav h1 {
    font-family: "Raleway", sans-serif;
    color: var(--beige);
    text-transform: uppercase;
    font-size: 40px;
    letter-spacing: -4px;
    margin-top: 2vh;
  }

  .mobile-nav p {
    font-family: "Raleway", sans-serif;
    color: var(--beige);
    text-transform: uppercase;
    font-size: 40px;
    margin-top: 2vh;
    font-weight: bold;
  }

  ul {
    width: 100%;
    flex-direction: column;
    padding: 0;
  }

  li {
    color: var(--beige);
    font-size: 30px;
    padding-top: 30px;
  }

  .first {
    animation: nav-animation 0.2s;
  }

  .second {
    animation: nav-animation 0.4s;
  }

  .third {
    animation: nav-animation 0.6s;
  }

  .fourth {
    animation: nav-animation 0.8s;
  }

  .last {
    animation: nav-animation 1s;
  }
}
</style>