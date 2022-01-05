<template>
  <main class="main">
    <div class="main__container _container">
      <Title></Title>
      <Projects></Projects>
      <Technologies></Technologies>
      <About></About>
    </div>
  </main>
</template>

<script>
import Title from "./Main-title.vue";
import Projects from "../Projects/Projects.vue";
import Technologies from "@/Technologies/Technologies.vue";
import About from "../About/About.vue";
export default {
  data: () => {
    return {
      title: "",
      text: "",
    };
  },
  components: {
    Title,
    Projects,
    Technologies,
    About,
  },
};
</script>

<style lang="scss" scoped>
.main__container {
  max-width: 800px;
  margin: 0 auto;

  position: relative;
}
main {
  margin-top: 70px;
  flex: 1 1 auto;
}
</style>
