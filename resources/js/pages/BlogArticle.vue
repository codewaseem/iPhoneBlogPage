<template>
  <div class="blog-article">
    <blog-header
      class="blog-header"
    >10 Best Photo Apps For Incredible iPhone Photography (2020 Edition)</blog-header>
    <div class="empty-grid-box"></div>
    <blog-post class="blog-post"></blog-post>
    <side-bar class=".side-bar"></side-bar>
  </div>
</template>

<script>
import BlogPost from "../components/BlogPost";
import SideBar from "../components/SideBar";
import BlogHeader from "../components/BlogHeader";

export default {
  components: {
    BlogPost,
    SideBar,
    BlogHeader
  }
};
</script>

<style lang="scss" scoped>
@import "../../sass/mixins";
.blog-article {
  margin: auto;

  .blog-header,
  .blog-post {
    max-width: 560px;
    margin: auto;
    /* margin-bottom: 0; */
  }

  .side-bar {
    max-width: 340px;
  }

  @include desktop-styles {
    width: 890px;

    @supports (display: grid) {
      display: grid;
      grid-template-columns: 560px 270px;
      grid-column-gap: 55px;
    }

    display: flex;
    flex-wrap: wrap;
    margin: auto;

    .side-bar {
      max-width: 270px;
      margin-top: 0;
      margin-right: 0;
      height: 640px;
    }
    .blog-header {
      margin-top: 76px;
      font-size: 26px;
      line-height: 31px;
    }

    .blog-post {
      margin-bottom: 130px;
    }

    .blog-header,
    .blog-post {
      margin-left: 0;
      margin-right: 0;
    }
  }
}
</style>
