<template>
  <section class="main-first">
    <div class="text">
      <div>
        <p class="hello">Hallå där! <span>&#128075;</span></p>
        <h2>
          Mitt namn är <span>Jessica Haara.</span><br />
          Jag håller på med <br />
          <span>frontendutveckling.</span>
        </h2>
      </div>
      <p class="more">Vill du veta mer?</p>
      <div class="buttons">
        <GreenButton
          v-bind:buttonTitle="'läs Om mig'"
          @click.native="scrollToAbout()"
        />
        <GreenButton
          v-bind:buttonTitle="'se Mitt cv'"
          @click.native="openResume()"
          class="resume-button"
        />
      </div>
    </div>

    <div class="avatar"></div>
  </section>
</template>

<script>
import GreenButton from "../buttons/GreenButton.vue";
export default {
  components: {
    GreenButton,
  },

  methods: {
    openResume() {
      window.open("/JessicaHaaraCV.pdf", "_blank");
    },
    scrollToAbout() {
      this.$emit("scrollclick", "about");
    },
  },
};
</script>

<style scoped>
.main-first {
  width: 80%;
  height: 80vh;
  display: flex;
  justify-content: space-between;
  margin: 80px auto 0 auto;
  align-items: center;
}

.text {
  height: 32vw;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

p {
  font-family: "Raleway", sans-serif;
  margin: 0;
  font-size: 4vh;
  position: relative;
  color: var(--almost-black);
}

.hello {
  animation: hello-animation 1s;
}

p span {
  display: inline-block;
  transform-origin: 70% 70%;
  animation: waving-hand 2s;
  transition: 0.2s;
}

p span:hover {
  display: inline-block;
  transform: rotate(45deg);
}

h2 {
  font-family: "Assistant", sans-serif;
  font-weight: bold;
  font-size: 4vw;
  color: var(--almost-black);
  margin: 0;
  animation: text-animation 1s;
  position: relative;
}

h2 span {
  color: var(--green);
}

h2 span:hover {
  -webkit-text-fill-color: transparent;
  -webkit-text-stroke-width: 0.5px;
  -webkit-text-stroke-color: var(--green);
}

.more {
  margin-top: 5vh;
  animation: text-animation 1.5s;
}

.buttons {
  display: flex;
  animation: text-animation 2s;
}

.resume-button {
  margin-left: 30px;
}

.avatar {
  height: 32vw;
  width: 30vw;
  background: url("~@/assets/avatar.jpg") no-repeat;
  background-position: center;
  background-size: cover;
  transition: 0.3s;
  animation: avatar-opacity 1s;
}

.avatar:hover {
  background: url("~@/assets/avatar-hover.jpg") no-repeat;
  background-position: center;
  background-size: cover;
}

@keyframes avatar-opacity {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

@keyframes hello-animation {
  0% {
    top: -30vh;
    opacity: 0;
  }

  10% {
    opacity: 1;
  }

  20% {
    top: 10px;
  }

  40% {
    top: -10px;
  }

  60% {
    top: 5px;
  }

  80% {
    top: -5px;
  }

  90% {
    top: 2px;
  }

  100% {
    top: 0;
  }
}

@keyframes text-animation {
  0% {
    opacity: 0;
    top: 10vh;
  }

  30% {
    opacity: 0;
    top: 10vh;
  }

  40% {
    opacity: 0.5;
  }

  100% {
    opacity: 1;
    top: 0;
  }
}

@keyframes waving-hand {
  0% {
    transform: rotate(0deg);
  }

  20% {
    transform: rotate(15deg);
  }

  40% {
    transform: rotate(-10deg);
  }

  60% {
    transform: rotate(15deg);
  }

  80% {
    transform: rotate(-10deg);
  }

  100% {
    transform: rotate(0deg);
  }
}

@media only screen and (max-width: 852px) {
  .main-first {
    flex-direction: column;
    align-items: center;
    width: 90%;
    height: auto;
    min-height: 85vh;
  }

  h2 {
    font-size: 7vw;
  }

  p {
    font-size: 6vw;
  }
  .text {
    height: auto;
  }

  .avatar {
    width: 60vw;
    height: 80vw;
    background-position: right center;
    margin-top: 10px;
  }

  .buttons {
    flex-direction: column;
    align-items: flex-start;
    margin-top: 10px;
  }

  .resume-button {
    margin-top: 20px;
    margin-left: 0;
  }
}
</style>