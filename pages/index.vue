<template>
  <div>
    <Header />
    <Aside :isShowMobileMenu="isShowMobileMenu" />
    <!--<Header />
    <Aside />-->
    <Content />
  </div>
</template>

<script>
import Header from "@/components/home/Header";
import Aside from "@/components/home/Aside";
import Content from "@/components/home/Content";
export default {
  components: {
    Aside,
    Content,
    Header,
  },
  data() {
    return {
      isShowMobileMenu: false,
    };
  },
  created() {
    this.$nuxt.$on("isShowMenu", ($event) => {
      this.isShowMobileMenu = $event;
    });
  },
};
</script>

<style lang="scss">
</style>
