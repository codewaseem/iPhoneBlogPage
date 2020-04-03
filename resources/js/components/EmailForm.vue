
<template>
  <form class="form" @submit.prevent="onSubmit">
    <label :class="{invalid : isInvalidEmail}" class="has-float-label">
      <input placeholder="mail@example.com" v-model="email" />

      <!--  Email Regex:  https://regex101.com/r/mX1xW0/1 -->

      <span>{{placeholder}}</span>
    </label>
    <cta-button
      class="font-styles btn-hover"
      @submit.native.prevent="window.reload"
    >Send Me The Tips »</cta-button>
  </form>
</template>

<script>
import CtaButton from "./CtaButton";

function isValidEmail(email) {
  return !!email.match(
    /^([\w-]+(?:\.[\w-]+)*)@((?:[\w-]+\.)*\w[\w-]{0,66})\.([a-z]{2,6}(?:\.[a-z]{2})?)$/i
  );
}

export default {
  data() {
    return {
      placeholder: "Please enter your email here",
      email: "",
      isInvalidEmail: false
    };
  },
  methods: {
    onSubmit() {
      if (!isValidEmail(this.email)) {
        this.placeholder = "Please enter a valid email address";
        this.isInvalidEmail = true;
      } else {
        location.reload();
      }
    }
  },
  components: {
    CtaButton
  }
};
</script>

<style lang="scss" scoped>
@import "../../sass/mixins";
@import "../../sass/float-lable";

.form {
  @include element("form-field") {
    position: relative;
  }
}

.font-styles {
  font-size: 18px;
  line-height: 22px;
}

.btn-hover:hover {
  background: linear-gradient(90deg, #b678aa 1.29%, #e28990 100%);
}

.has-float-label {
  @include float-label-container;

  @include float-label;

  &.invalid {
    border: 1px solid #e51323;

    input {
      color: #e51323;
      & + span {
        color: #e51323;
      }
    }
  }

  input {
    @include float-label-input;
    border: 0;
    position: absolute;
    left: 16px;
    top: 26px;
    color: #000000;
    font-weight: 300;
    font-size: 16px;
    line-height: 19px;
    bottom: 8px;

    @include float-label-scaled {
      color: #828282;
      top: 50%;
      transform: translateY(-50%);
      font-weight: 300;
      font-size: 18px;
      line-height: 22px;
    }

    &:focus {
      outline: none;
      border-color: rgba(0, 0, 0, 0.5);
    }
  }
}
</style>