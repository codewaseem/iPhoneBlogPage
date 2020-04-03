<template>
  <aside class="side-bar">
    <cta-button @click.native="openPopup" :style="{width:'283px'}">Send Me The Tips</cta-button>
    <popup-form v-if="isPopupOpen" @close="closePopup"></popup-form>
  </aside>
</template>

<script>
import CtaButton from "./CtaButton";
import PopupForm from "./PopupForm";
export default {
  data() {
    return { isPopupOpen: false };
  },
  methods: {
    openPopup() {
      this.isPopupOpen = true;
      //prevent scrolling when pop-up is open
      window.document.body.style.overflow = "hidden";
    },
    closePopup() {
      this.isPopupOpen = false;
      // allow normal scroll behaviour when pop-up is closed
      window.document.body.style.overflow = "";
    }
  },
  components: {
    CtaButton,
    PopupForm
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
