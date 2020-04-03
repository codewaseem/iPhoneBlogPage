<template>
  <button class="cta-btn">
    <slot></slot>
  </button>
</template>



<style lang="scss" scoped>
.cta-btn {
  background: linear-gradient(90deg, #ac519c 0.83%, #e5424f 100%);
  margin: auto;
  position: relative;
  font-weight: bold;
  font-size: 20px;
  line-height: 24px;
  /* identical to box height */
  cursor: pointer;
  border: 0px;
  text-align: center;
  display: block;
  color: #ffffff;
  width: 100%;
  font-family: Lato;
  height: 50px;

  &:hover,
  &:focus {
    box-shadow: 0px 3px 10px rgba(104, 104, 104, 0.5);
  }
}
</style>