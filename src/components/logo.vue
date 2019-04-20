<template>
  <div class="logo">
    <img src="/src/assets/logo.png" alt="logo" title="JK-World">
  </div>
</template>

<script>
export default {
  name: "logo",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
img {
  max-width: 100%;
  height: auto;
}
.logo {
  border-bottom: 5px dotted #a9a9a9;
}
</style>
