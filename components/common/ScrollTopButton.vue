<template>
  <div
    ref="scrollTopButton"
    class="sticky w-full flex justify-end bottom-0 pb-3 pr-5 transition"
  >
    <div
      v-on:click="scrollToTop"
      class="text-white hover:text-blue-400 transition"
    >
      <button class="scrollTopButton">
        <img src="/up_icon.svg" style="height: 20px; padding-left: 17.5px" />
      </button>
    </div>
  </div>
</template>

<script>
import * as Vue from "vue";

export default {
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },

  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },

  methods: {
    handleScroll() {
      const scrollBtn = this.$refs.scrollTopButton;

      if (window.scrollY > 0) {
        scrollBtn.classList.remove("invisible");
      } else {
        scrollBtn.classList.add("invisible");
      }
    },
    scrollToTop() {
      window.scrollTo(0, 0);
    },
  },
};
</script>

<style>
html {
  scroll-behavior: smooth;
}
.scrollTopButton {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  font-size: 1.5rem;
  background: #ffc72c;
  box-shadow: 0px 1px 5px rgba(0, 0, 0, 0.2), 0px 3px 4px rgba(0, 0, 0, 0.12),
    0px 2px 4px rgba(0, 0, 0, 0.14);
}
</style>
