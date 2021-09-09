<template>
  <div class="content-left">
    <h1>All activity</h1>
    <Repo />
    <Button />
    <Footer />
  </div>
</template>

<script>
import Repo from "@/components/content/homepage/Repo";
import Button from "@/components/content/homepage/Button";
import Footer from "@/components/content/homepage/Footer";
export default {
  components: {
    Repo,
    Button,
    Footer,
  },
};
</script>