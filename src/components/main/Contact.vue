<template>
  <section class="contact">
    <h2><span>3.</span> Kontakt</h2>
    <div class="flex">
      <div class="contact-info">
        <p>Vill du komma i kontakt med mig?</p>
        <p>
          Det gör du det enkelt genom att använda mitt fina formulär här på
          sidan.
        </p>
      
        <p>
          Du får även gärna connecta med mig på
          <a href="https://www.linkedin.com/in/jessica-haara/" target="_blank"
            >LinkedIn</a
          >!
        </p>

        <p>Hoppas vi hörs!</p>
      </div>
      <div class="contact-form">
        <form
          action="https://formsubmit.co/cc2951ecb4af60470dc8054a663d9be5"
          method="POST"
        >
          <input type="text" name="name" placeholder="Ditt namn" required />

          <input type="email" name="email" placeholder="Din e-post" required />

          <input type="text" name="subject" placeholder="Ämne" required />

          <textarea
            placeholder="Meddelande"
            class="form-control"
            name="message"
            rows="10"
            required
          ></textarea>
          <button type="submit">Skicka</button>
        </form>
      </div>
    </div>
  </section>
</template>


<script>
export default {};
</script>

<style scoped>
.contact {
  width: 100%;
  min-height: 100vh;
  margin: 0 auto;
}

.flex {
  display: flex;
  margin-top: 20px;
}

.contact-info {
  margin-left: 10%;
  padding-right: 40px;
}

p {
  font-family: "Raleway", sans-serif;
  color: var(--almost-black);
  font-size: 4vh;
}

a {
  font-family: "Raleway", sans-serif;
  color: var(--pink);
  font-size: 4vh;
  font-weight: bold;
}

a:hover {
  color: var(--almost-black)
}
.contact-info,
.contact-form {
  width: 50%;
  height: 80vh;
}

.contact-form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

h2 {
  font-family: "Raleway", sans-serif;
  color: var(--almost-black);
  font-size: 5vh;
  text-transform: uppercase;
  margin-bottom: 2vh;
  animation: hide-h2 4s;
  margin-left: 10vw;
}

h2 span {
  color: var(--green);
}

form {
  width: 100%;
  height: 500px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}

input,
textarea {
  width: 60%;
  font-family: "Assistant", sans-serif;
  padding-left: 10px;
  font-size: 1.1em;
  border: 0.5px solid var(--almost-black);
  color: var(--almost-black);
}

input {
  height: 50px;
}

textarea {
  height: 200px;
  padding-top: 10px;
}

button {
  font-family: "Raleway", sans-serif;
  color: var(--green);
  text-transform: uppercase;
  font-size: 16px;
  font-weight: bold;
  padding: 15px 30px;
  border: 2px solid var(--green);
  background-color: var(--green);
  background-image: linear-gradient(90deg, var(--green) 50%, #fff 50%);
  background-position: 100%;
  background-size: 400%;
  transition: background-position 250ms ease-in-out;
  cursor: pointer;
  margin-bottom: 10px;
}

button:hover {
  background-position: 0;
  color: #fff;
}

@media only screen and (max-width: 852px) {
  .flex {
    flex-direction: column;
  }

  .contact-info {
    padding: 0;
    margin-bottom: 30px;
    width: 80%;
  }

  .contact-info,
  .contact-form {
    height: auto;
  }

  .contact-form {
    width: 100%;
  }
}
</style>