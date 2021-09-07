<template>
  <div>
    <Aside />
    <Content />
  </div>
</template>

<script>
import Aside from "@/components/home/Aside";
import Content from "@/components/home/Content";
export default {
  layout: "Common",
  components: {
    Aside,
    Content,
  },
};
</script>

<style lang="scss">
</style>
