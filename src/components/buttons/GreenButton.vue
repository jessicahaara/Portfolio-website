<template>
  <button>{{ buttonTitle }} <span>&#8594;</span></button>
</template>

<script>
export default {
  props: {
    buttonTitle: String,
  },
};
</script>

<style scoped>
button {
  font-family: "Raleway", sans-serif;
  color: var(--green);
  text-transform: uppercase;
  font-size: 16px;
  font-weight: bold;
  padding: 15px 30px;
  border: 2px solid var(--green);
  display: flex;
  align-items: center;
  cursor: pointer;
  transition: margin 0.4s linear;
  justify-content: center;
  background-image: linear-gradient(90deg, var(--green) 50%, var(--beige) 50%);
  background-position: 100%;
  background-size: 400%;
  transition: background-position 250ms ease-in-out;
  width: 200px;
}

button:hover {
  background-position: 0;
  color: #fff;
  padding-right: 10px;
}

button span {
  font-size: 20px;
  margin-left: 15px;
  margin-bottom: 2px;
}

button:hover span {
  margin-left: 35px;
}

@media only screen and (max-width: 930px) {
  button {
    padding: 10px 30px;
    width: 200px;
  }
}
</style>