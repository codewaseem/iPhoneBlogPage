<template>
  <div class="popup">
    <div class="popup_overlay"></div>
    <div class="popup__container">
      <div class="popup__close" @click="$emit('close')">×</div>
      <div class="progress">
        <span class="progress__step-count">Step 1 of 2</span>
        <div class="progress__meter">
          <div class="progress__bar"></div>
        </div>
      </div>
      <section class="form-section">
        <h3 class="form-section__heading">
          Enter Your Email To Get
          <span class="form-section_green-text">FREE</span> iPhone Photography
          Email Tips:
        </h3>
        <form class="form">
          <email-field></email-field>
          <cta-button @submit.native.prevent="window.reload">Send Me The Tips »</cta-button>
        </form>
      </section>
    </div>
  </div>
</template>

<script>
import EmailField from "./EmailField";
import CtaButton from "./CtaButton";

export default {
  components: {
    EmailField,
    CtaButton
  },
  mounted() {
    console.log("Component mounted.");
  }
};
</script>

<style lang="scss" scoped>
@import "../../sass/mixins";

.popup {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100vw;

  @include modifier("overlay") {
    position: absolute;
    height: 100%;
    width: 100%;
    background: #262626;
    mix-blend-mode: normal;
    opacity: 0.8;
  }

  @include element("close") {
    position: absolute;
    height: 35px;
    right: 9px;
    font-family: Lato;
    font-style: normal;
    font-weight: bold;
    font-size: 29px;
    line-height: 35px;
    /* identical to box height */
    z-index: 999;
    color: #464646;
    cursor: pointer;
  }

  @include element("container") {
    position: relative;
    width: 355px;
    padding-bottom: 24px;
    margin: auto;
    background: #ffffff;
    box-shadow: 0px 0px 60px rgba(0, 0, 0, 0.5);
    display: flex;
    flex-direction: column;
    top: 50%;
    transform: translateY(-50%);
  }

  .form-section {
    width: 320px;
    margin: 0 auto;

    @include modifier("green-text") {
      color: #427b09;
    }
    @include element("heading") {
      font-weight: bold;
      font-size: 20px;
      line-height: 26px;
      margin-bottom: 23px;
      color: #464646;
    }
  }

  .form {
    @include element("form-field") {
      position: relative;
    }
  }

  .progress {
    width: 320px;
    margin: 12px auto;
    margin-bottom: 20px;
    text-align: center;

    @include element("step-count") {
      font-style: normal;
      font-weight: 300;
      font-size: 14px;
      line-height: 17px;
      color: #848484;
      display: inline-block;
      margin-bottom: 12px;
    }

    @include element("meter") {
      position: relative;
      width: 100%;
      height: 2px;
      background: #e5e5e5;
    }

    @include element("bar") {
      position: absolute;
      top: 0px;
      left: 0px;
      width: 50%;
      height: 2px;
      background: linear-gradient(90deg, #e5424f 20%, #ac519c);
    }
  }
}
</style>
