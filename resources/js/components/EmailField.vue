
<template>
  <label class="has-float-label">
    <!--  Email Regex:  https://regex101.com/r/mX1xW0/1 -->
    <input
      pattern="^([\w-]+(?:\.[\w-]+)*)@((?:[\w-]+\.)*\w[\w-]{0,66})\.([a-z]{2,6}(?:\.[a-z]{2})?)$"
      placeholder="mail@example.com"
      v-on:input="checkEmail"
    />
    <span>{{placeholder}}</span>
  </label>
</template>

<script>
export default {
  data() {
    return {
      placeholder: "Please enter your email here"
    };
  },
  methods: {
    checkEmail(event) {
      let { validity } = event.target;
      if (validity.patternMismatch) {
        this.placeholder = "Please enter a valid email address";
      } else {
        this.placeholder = "Please enter your email here";
      }
    }
  },
  mounted() {
    console.log("Component mounted.");
  }
};
</script>

<style lang="scss" scoped>
@import "../../sass/mixins";

.has-float-label {
  @include float-label-container;

  @include float-label;

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