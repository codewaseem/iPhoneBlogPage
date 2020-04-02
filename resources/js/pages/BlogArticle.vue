<template>
    <div>
        <blog-post></blog-post>
        <popup-form v-show="showPopup"></popup-form>
    </div>
</template>

<script>
import BlogPost from "../components/BlogPost";
import PopupForm from "../components/PopupForm";

export default {
    data() {
        return {
            showPopup: false
        };
    },
    components: {
        BlogPost,
        PopupForm
    }
};
</script>
