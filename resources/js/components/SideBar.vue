<template>
    <aside class="side-bar">
        <button class="side-bar__cta-btn">
            Send Me The Tips
        </button>
    </aside>
</template>

<script>
export default {
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

    @include element("cta-btn") {
        background: linear-gradient(90deg, #ac519c 0.83%, #e5424f 100%);
        /* box-shadow: 0px 3px 10px rgba(104, 104, 104, 0.5); */
        margin: auto;
        position: relative;
        font-weight: bold;
        font-size: 20px;
        line-height: 24px;
        /* identical to box height */
        border: 0px;
        text-align: center;
        display: block;
        color: #ffffff;
        width: 283px;
        font-family: Lato;
        height: 49px;
    }
}
</style>
