<template>
  <section class="about">
    <div class="space"></div>
    <h2><span>1.</span> Om mig</h2>
    <p>
      "Efter Covid-19 kommer <span>kodning 2021</span>", lyder inget ordspråk.
      Men pandemin medförde ett nytt karriärsval för mig åtminstone. Jag har
      tidigare utbildat mig till <span>digital analytiker </span>men blev
      kortvarig i den världen innan jag insåg att kodning var roligare. Men
      självklart tycker jag fortfarande analys är både viktigt och intressant.
      Att jag drogs mer till koden tror jag har att göra med min
      <span>förkärlek till problemlösning</span>. Det märks då jag på fritiden
      gärna lägger pussel, löser suduko och utmanar vänner i spel (både brädspel
      och datorspel). <br /><br />Programmering är verkligen något jag brinner
      för och det vet jag eftersom att jag kan komma på mig själv med att sitta
      med nya <span>kodningsprojekt</span>. Ofta alldeles för sent på kvällarna
      på fritiden. Det händer oftare än jag vill erkänna att jag även ligger
      sömnlös och funderar på hur jag ska lösa olika problem som uppstått i
      koden under dagen. <br /><br />
      Förutom när jag programmerar så mår jag bra av min familj, som består av
      en sambo, två barn och en liten hund. Jag gillar också att vara ute i
      naturen, läsa någon spännande bok, lyssna på en bra podd i bilen eller åka
      och kolla på när <span>Djurgården vinner fotbollsmatcher.</span> Och
      precis som många andra gillar även jag att sitta lite för länge i soffan
      och kolla TV-serier.
    </p>

    <p class="no-border">
      Vill du veta mer kan du kolla in mitt
      <span class="link"
        ><a href="/JessicaHaaraCV.pdf" target="_blank">CV</a></span
      >
      eller <span class="link" @click="toContact()"> kontakta mig</span> för
      frågor.
    </p>
  </section>
</template>

<script>
export default {
  methods: {
    toContact() {
      this.$emit("toContact", "contact");
    },
  },
};
</script>

<style scoped>
.about {
  width: 80%;
  min-height: 100vh;
  margin: 0 auto;
}

.space {
  height: 30px;
}

h2 {
  font-family: "Raleway", sans-serif;
  color: var(--almost-black);
  font-size: 5vh;
  text-transform: uppercase;
  margin-bottom: 2vh;
}

h2 span {
  color: var(--green);
}

p {
  margin-top: 0;
  width: 100%;
  font-size: 3.5vh;
  font-family: "Assistant", sans-serif;
  border-left: 4px solid var(--green);
  padding-left: 1vw;
}

p span {
  color: var(--green);
  font-weight: bold;
}

.no-border {
  border-left: none;
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

@media only screen and (max-width: 852px) {
  .space {
    height: 20px;
  }

  p {
    border-left: 0px;
    font-size: 2.5vh;
  }
}
</style>