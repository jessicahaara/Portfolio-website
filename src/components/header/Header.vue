<template>
  <div class="header">
    <Name />
    <Nav @scrollclick="scroll" />
  </div>
</template>

<script>
import Name from "./Name.vue";
import Nav from "./Nav.vue";
export default {
  components: {
    Name,
    Nav,
  },

  methods: {
    scroll(id) {
      this.$emit("scrollclick", id);
    },
  },
};
</script>

<style scoped>
.header {
  width: 90%;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 80px;
}
</style>