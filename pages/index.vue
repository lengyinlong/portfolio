<template>
  <div>
    <Navbar />
    <Content />
    <ScrollTopButton />
    <Footer />

    <Template />
  </div>
</template>

<script>
import Navbar from "~~/components/Navbar.vue";
import Content from "~~/components/Content.vue";
import Footer from "~~/components/Footer.vue";
import ScrollTopButton from "~~/components/common/ScrollTopButton.vue";
import Template from "~~/components/Template.vue";

export default {
  name: "IndexPage",
};
</script>
