<template>
  <header class="blog-header">
    <h2 class="blog-header__title">
      <slot></slot>
    </h2>

    <svg
      class="blog-header__divider"
      width="100%"
      viewBox="0 0 340 2"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M1.47753 1.5H340.522"
        stroke="url(#paint0_linear)"
        stroke-width="2"
        stroke-linecap="square"
      />
      <defs>
        <linearGradient id="paint0_linear" gradientUnits="userSpaceOnUse">
          <stop offset="0.000923775" stop-color="#9B2686" />
          <stop offset="1" stop-color="#E51323" />
        </linearGradient>
      </defs>
    </svg>
  </header>
</template>

<style lang="scss" scoped>
@import "../../sass/mixins";

.blog-header {
  > * {
    @include default-section-style;
    @include desktop-styles {
      width: 100%;
    }
  }

  @include element("divider") {
    display: block;
    margin: 0 auto;
  }

  @include element("title") {
    font-size: 24px;
    line-height: 29px;
    font-weight: bold;

    @include desktop-styles {
      font-size: 26px;
      line-height: 31px;
    }
  }
}
</style>