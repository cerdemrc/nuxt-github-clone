<template>
  <div>
    <Header />
    <Aside />
    <Nuxt />
  </div>
</template>

<script>
import Header from "@/components/common/Header";
import Aside from "@/components/home/Aside";
export default {
  components: {
    Header,
    Aside,
  },
};
</script>

<style lang="scss">
</style>