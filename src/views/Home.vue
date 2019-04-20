<template>
  <div class="home">
    <HelloWorld msg="歡迎光臨"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>

<style scoped lang="scss">
.home {
  background-color: #d3d3d3;
}
</style>
