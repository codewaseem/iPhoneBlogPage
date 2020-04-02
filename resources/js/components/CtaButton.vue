<template>
  <button class="cta-btn">
    <slot></slot>
  </button>
</template>

<script>
export default {
  mounted() {
    console.log("Component mounted.");
  }
};
</script>

<style lang="scss" scoped>
.cta-btn {
  background: linear-gradient(90deg, #ac519c 0.83%, #e5424f 100%);
  /* box-shadow: 0px 3px 10px rgba(104, 104, 104, 0.5); */
  margin: auto;
  position: relative;
  font-weight: bold;
  font-size: 20px;
  line-height: 24px;
  /* identical to box height */
  border: 0px;
  text-align: center;
  display: block;
  color: #ffffff;
  width: 100%;
  font-family: Lato;
  height: 50px;
}
</style>