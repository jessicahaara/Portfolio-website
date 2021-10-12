<template>
  <section class="contact">
    <h2><span>4.</span> Kontakt</h2>
    <form
      action="https://formsubmit.co/cc2951ecb4af60470dc8054a663d9be5"
      method="POST"
    >
      <label for="name">Ditt namn:</label>
      <input type="text" name="name" required />
      <label for="email">Din e-post:</label>
      <input type="email" name="email" required />
      <label for="message">Meddelande:</label>
      <textarea
        placeholder="Your Message"
        class="form-control"
        name="message"
        rows="10"
        required
      ></textarea>
      <button type="submit">Skicka</button>
    </form>
  </section>
</template>


<script>
export default {};
</script>

<style scoped>
.contact {
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
</style>