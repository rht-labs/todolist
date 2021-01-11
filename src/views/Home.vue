<template>
  <div class="home">
    <img
      class="banner-image"
      src="https://www.redhat.com/outfit/b64444a376f6be2a8ee78f111930a2aa/Logo-Red_Hat-Open_Innovation_Labs-A-Standard-RGB.png"
      width="330px"
    />
    <h1>Welcome 👋</h1>
    <AboutLabs />
  </div>
</template>

<script>
// @ is an alias to /src
import AboutLabs from "@/components/AboutLabs.vue";

export default {
  name: "home",
  components: {
    AboutLabs
  }
};
</script>
<style scoped>
.banner-image {
  padding-bottom: 20px;
  padding-top: 20px;
}
</style>
