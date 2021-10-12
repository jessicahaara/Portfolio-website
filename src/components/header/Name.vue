<template>
  <section class="name">
    <h1></h1>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
h1:before {
  content: "JH";
  /* animation: h1-animation 3s; */
}

h1 {
  font-family: "Raleway", sans-serif;
  color: var(--almost-black);
  animation: nav-animation 0.2s;
  font-size: 40px;
  letter-spacing: -4px;
  transition: 0.2s;
  margin: 0;
}

h1:hover {
  color: var(--green);
  margin-top: -5px;
  cursor: pointer;
}

@keyframes h1-animation {
  0% {
    content: "Jessica Haara";
    opacity: 0;
  }

  55% {
    content: "Jessica Haara";
  }

  60% {
    color: var(--almost-black);
    content: "Jessica Haara";
    opacity: 1;
  }

  65% {
    content: "Jessic Haar";
  }

  70% {
    content: "Jessi Haa";
  }

  75% {
    content: "Jess Ha";
  }

  80% {
    content: "Jes H";
  }

  85% {
    content: "Je H";
    text-align: center;
  }

  90% {
    content: "JH";
    letter-spacing: 4px;
  }

  100% {
    letter-spacing: -4px;
    font-size: 40px;
  }
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

@media only screen and (max-width: 768px) {
}
</style>