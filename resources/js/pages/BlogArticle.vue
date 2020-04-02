<template>
  <div>
    <blog-post></blog-post>
    <side-bar></side-bar>
    <popup-form></popup-form>
  </div>
</template>

<script>
import BlogPost from "../components/BlogPost";
import SideBar from "../components/SideBar";
import PopupForm from "../components/PopupForm";

export default {
  components: {
    BlogPost,
    SideBar,
    PopupForm
  }
};
</script>
