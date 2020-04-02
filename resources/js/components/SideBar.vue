<template>
  <aside class="side-bar">
    <cta-button :style="{width:'283px'}">Send Me The Tips</cta-button>
  </aside>
</template>

<script>
import CtaButton from "./CtaButton";
export default {
  components: {
    CtaButton
  },
  mounted() {
    console.log("Component mounted.");
  }
};
</script>

<style lang="scss" scoped>
@import "../../sass/mixins";

.side-bar {
  width: 340px;
  height: 426px;
  background: #f5f5f5;
  margin: 33px auto 37px;
  padding-top: 34px;
}
</style>
