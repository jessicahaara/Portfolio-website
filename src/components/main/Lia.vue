<template>
  <section class="lia">
    <h2><span>2.</span> Lia 2022</h2>
    <section class="lia-content">
      <section class="lia-text">
        <p>
          Just nu letar jag efter en praktikplats där jag kan påbörja min
          arbetsmässiga <span>karriär som problemlösare.</span>
        </p>

        <p>
          I <span>januari 2022</span> så ska jag göra praktik inom
          frontendutveckling. Praktikperioden är på heltid i
          <span>20 veckor</span> och efter de 20 veckorna kommer jag vara klar
          med min utbildning.
        </p>

        <p>
          Jag vill hitta en praktik där jag får jobba i ett roligt team och
          gärna med <span>fokus på JavaScript</span>, med eller utan ramverk
          spelar ingen roll!
        </p>

        <p>
          Har du en plats som du tror skulle passa mig eller har nåt tips på
          något företag så
          <span class="link" @click="toContact()">hör av dig!</span>
        </p>
      </section>

      <img src="~@/assets/avatar-hover.jpg" alt="" />
    </section>
  </section>
</template>

<script>
export default {
  methods: {
    toContact() {
      this.$emit("scrollclick", "contact");
    },
  },
};
</script>

<style scoped>
.lia {
  width: 80%;
  min-height: 100vh;
  margin: 0 auto;
}

.lia-content {
  display: flex;
  justify-content: space-between;
}

h2 {
  font-family: "Raleway", sans-serif;
  color: var(--almost-black);
  font-size: 5vh;
  text-transform: uppercase;
  margin-bottom: 2vh;
  animation: hide-h2 4s;
}

h2 span {
  color: var(--green);
}

p {
  font-size: 3.5vh;
  font-family: "Assistant", sans-serif;
}

p span {
  color: var(--green);
  font-weight: bold;
}

.lia-text {
  width: 50%;
}

img {
  width: 40%;
  height: 40%;
  align-self: flex-end;
}

.link,
.link a {
  color: var(--pink);
  text-decoration: underline;
  cursor: pointer;
}

.link:hover,
.link a:hover {
  color: var(--almost-black);
}

@media only screen and (max-width: 1000px) {
  img {
    display: none;
  }

  .lia-text {
    width: 100%;
  }
}
</style>