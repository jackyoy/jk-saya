<template>
  <div class="Calculation">
    <div class="container">
      <div class="row">
        <div class="col align-self-center">
          <h1>這是一個計算機頁面</h1>
          <Gashapon></Gashapon>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import Gashapon from "@/components/Gashapon.vue";

export default {
  name: "Calculation",
  components: { Gashapon }
};
</script>
<style lang="scss" scoped>
.Calculation {
  background-color: #d3d3d3;
}
</style>

