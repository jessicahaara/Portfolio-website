<template>
  <button>{{ buttonTitle }}</button>
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
  color: var(--pink);
  text-transform: uppercase;
  font-size: 16px;
  font-weight: bold;
  padding: 10px 20px;
  border: 2.5px solid var(--pink);
  background-color: transparent;
  display: flex;
  align-items: center;
  cursor: pointer;
  transition: background-color 0.4s linear;
  transition: margin 0.4s linear;
  justify-content: center;
}

button:hover {
  background-color: var(--pink);
  color: #fff;
}

/* @media only screen and (max-width: 930px) {
	button {
		padding: 10px 30px;
	}
} */
</style>