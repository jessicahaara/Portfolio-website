<template>
  <section class="projects">
    <h2><span>3.</span> Projekt</h2>

    <h4>
      Här nedan är några av projekten jag gjort på senaste tiden. Fler kommer
      inom kort.
    </h4>

    <article>
      <a
        href="https://fullstack-hamsterwars-jessica.herokuapp.com/"
        target="_blank"
      >
        <img src="@/assets/hamsterwars.jpg" alt="bild på hamsterwars hemsida"
      /></a>
      <div class="text">
        <h3>Hamsterwars (endast desktop)</h3>
        <p>
          En hemsida där två slumpmässigt utvalda hamstrar tävlar mot varandra i
          gullighet. Det finns ett galleri där man kan se alla tillgängliga
          hamstrar. I galleriet kan man även få mer information om hamstrarna
          och se statistik. Utöver det finns även en lista på de senast utförda
          tävlingarna och en sida med statistik över de som vunnit/förlorat
          mest.
        </p>
        <p>
          Uppgiften innebar att jag skulle bygga upp både
          <span>backend</span> och <span>frontend.</span> Med
          <span>Node.js</span> satte jag upp en utvecklingsmiljö för
          fullstackutveckling. Jag byggde ett <span>REST API</span> med
          <span>express</span> som hämtade och ändrade data från
          <span>firestore</span> (en molnbaserad databas). Sedan byggde jag en
          frontenddel i <span>React</span> till API:et. Navigering är gjort med
          <span>React Router</span> Jag använde mig av <span>Axios</span> för
          att skicka HTTP request. Hela appen är publicerad med
          <span>heroku.</span> Jag har själv designat applikationen. Tyvärr är
          inte sidan responsiv (ännu).
        </p>
        <p>
          <a
            href="https://fullstack-hamsterwars-jessica.herokuapp.com/"
            target="_blank"
          >
            Gå till Hamsterwars
          </a>
          eller
          <a
            href="https://github.com/jessicahaara/Hamsterwars-Project"
            target="_blank"
            >Se kod på GitHub</a
          >
        </p>
      </div>
    </article>

    <article class="reverse">
      <div class="text">
        <h3>Portfolio</h3>
        <p>
          Min egna hemsida som jag använder som min portfolio där jag kan
          berätta om mig själv och visa vad jag har gjort. Tanken är att
          hemsidan ska fungera som ett sätt att söka jobb, LIA och kontakter.
          Men den finns också här för att jag ska öva och kommer därför att
          ändras och optimeras hela tiden.
        </p>

        <p>
          Hemsidan har jag byggt i <span>Vue.js</span> men mycket fokus har
          legat i att fokusera på <span>HTML</span> och
          <span>CSS</span> eftersom jag i vanliga fall har lägger mycket tid på
          <span>JavaScript</span>. När jag utvecklat den här hemsidan har jag
          lagt mycket tid på att få en <span>interaktiv design</span> och att
          öva på <span>CSS animationer</span>. Men det har även varit viktigt
          att den är <span>responsiv</span>.
        </p>

        <p>
          <a
            href="https://github.com/jessicahaara/Portfolio-website"
            target="_blank"
            >Se kod på GitHub</a
          >
        </p>
      </div>
      <img src="@/assets/portfolio.jpg" alt="bild på portfolio hemsida" />
    </article>

    <article>
      <img src="@/assets/sinus.jpg" alt="bild på sinus hemsida" />
      <div class="text">
        <h3>Sinus Webshop</h3>
        <p>
          Sinus webshop är en sida där man kan köpa skateboards och relaterat.
          Det finns en sida där man kan registrera sig. Som registrerad
          användare kan man logga in på sidan för att se sina ordrar samt ändra
          uppgifter. Om man är inloggad när man skickar en beställning så fylls
          addresuppgifter in automatiskt. Man kan även logga in som Admin och då
          kan man se alla de senaste ordrarna. Som admin finns även ett
          CRUD-gränssnitt.
        </p>

        <p>
          Detta var en gruppuppgift där vi skulle öva på att jobba
          <span>agilt</span> och vi valde att jobba med <span>Scrum</span>. Vi
          byggde en frontendapplikation i <span>Vue.js</span> till en färdig
          backendlösning. Vi arbetade med state management i
          <span>Vuex</span> och använde <span>Vue Router</span> för navigation.
          Vi använde oss av <span>Axios</span> för att göra HTTP-request. Vissa
          delar av koden skrev vi tillsammans och andra delar delade vi upp.
          Designen gjorde vi efter en mockup och den är inte responsiv.
        </p>

        <p>
          <a
            href="https://github.com/jessicahaara/sinus-webshop"
            target="_blank"
            >Se kod på GitHub</a
          >
        </p>
      </div>
    </article>

    <article class="reverse">
      <div class="text">
        <h3>Photo search</h3>
        <p>
          Det här är en hemsida där jag använt mig av Unsplash API. På
          startsidan kommer det upp slumpmässigt utvalda bilder tills man väljer
          att söka på något. Sök resultatet kommer med 24 bilder per sida. Man
          kan bläddra mellan sidorna. Man kan även genom att klicka på en bild
          få upp en modal med vald bild. Där kan man bläddra genom bilderna i
          större storlek. Hovrar man över en bild kan man gilla den, ladda ner
          den, samt se vem bilden är tagen av. Det finns en vy där man kan se
          alla bilder man gillar och även ta bort bilder man gillat.
        </p>

        <p>
          Det här projektet startade jag dels för att träna på att använda mig
          av <span>API:er</span> men främst för att öva på
          <span>JavaScript</span> och <span>Vue.js</span> och att skicka data
          mellan komponenter. Jag sparar ner data i
          <span>localStorage</span> för att bilder man gillar ska kommas ihåg.
          Med Unsplash egna API kan jag hämta bilder utifrån vad användaren
          söker på samt ta fram slumpmässigt utvalda bilder. (länk kommer)
        </p>

        <p>
          <!-- <a href="http://unsplash-api.jessicahaara.com/" target="_blank">
            Gå till Unsplash API
          </a>
          eller -->
          <a href="https://github.com/jessicahaara/unsplah-api" target="_blank"
            >Se kod på GitHub</a
          >
        </p>
      </div>
      <!-- <a href="http://unsplash-api.jessicahaara.com" target="_blank"> -->
        <img src="@/assets/unsplash.jpg" alt="bild på photo search hemsida" />
      <!-- </a> -->
    </article>

    <article class="last">
      <a href="http://e-wallet.jessicahaara.com" target="_blank">
        <img src="@/assets/wallet.jpg" alt="bild på e-wallet hemsida" />
      </a>
      <div class="text">
        <h3>E-wallet</h3>
        <p>
          Det här är en digital plånbok med endast två vyer. En vy för att se
          och bläddra bland korten i den digitala plånboken. I den här vyn kan
          man även ta bort kort. På den andra vyn kan man lägga till nytt kort
          till plånboken.
        </p>

        <p>
          Det här var ett litet projekt som jag byggde i <span>Vue.js</span> och
          jag har använt <span>Vue Router</span> för navigation. Designen är
          gjord efter en mockup och alla kort är skapade med <span>CSS</span>.
          Det finns även en <span>validering</span> i formuläret för att lägga
          till ett nytt kort.
        </p>

        <p>
          <a href="http://e-wallet.jessicahaara.com/" target="_blank">
            Gå till E-wallet
          </a>
          eller
          <a
            href="https://github.com/jessicahaara/iths-e-wallet"
            target="_blank"
            >Se kod på GitHub</a
          >
        </p>
      </div>
    </article>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.projects {
  width: 80%;
  min-height: 100vh;
  margin: 0 auto;
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

h4 {
  font-family: "Assistant", sans-serif;
  color: var(--almost-black);
  font-size: 3.5vh;
  font-weight: normal;
}

article {
  margin-top: 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.text {
  width: 50%;
}

h3 {
  margin: 0;
  font-family: "Assistant", sans-serif;
  color: var(--almost-black);
  font-size: 4vh;
  text-transform: uppercase;
}

p {
  font-family: "Assistant", sans-serif;
  color: var(--almost-black);
  font-size: 1.15vw;
}

p span {
  color: var(--green);
  font-weight: bold;
}

a {
  font-family: "Raleway", sans-serif;
  color: var(--pink);
  cursor: pointer;
  font-weight: bold;
}

a:hover {
  color: var(--almost-black);
}

img {
  max-width: 80vw;
  opacity: 0.8;
  transition: 0.5 linear;
}

img:hover {
  opacity: 1;
}

.last {
  margin-bottom: 100px;
}

@media only screen and (max-width: 900px) {
  article {
    flex-direction: column;
  }

  .text {
    width: 80vw;
    order: 1;
  }

  .img {
    opacity: 1;
  }

  p {
    font-size: 15px;
  }
}
</style>