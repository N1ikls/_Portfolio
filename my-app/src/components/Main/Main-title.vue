<template>
  <div class="main__title">
    <h2>
      Welcome To <br />
      My Personal Portfolio
    </h2>
    <Text_body :text="text" />
    <Button :text="btn" />
    <Gradient_line />
  </div>
</template>

<script>
import Text_body from "@/Global/Components/Text.vue";
import Gradient_line from "../../Global/Components/Gradient_line.vue";
import Button from "../../Global/Components/Button.vue";
export default {
  data: () => {
    return {
      btn: "Learn More",
      text: " The purpose of JavaScript Mastery is to help aspiring and established developers to take their development skills to the next level and build awesome apps.",
    };
  },
  components: {
    Gradient_line,
    Button,
    Text_body,
  },
  name: "Main_title",
};
</script>

<style lang="scss">
.main__title {
  h2 {
    font-family: "Space Grotesk", sans-serif;
    font-weight: 800;
    font-size: 62px;
    line-height: 72px;
    width: max-content;
    max-width: 100%;
    background: linear-gradient(
      121.57deg,
      #ffffff 18.77%,
      rgba(255, 255, 255, 0.66) 60.15%
    );
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 16px;
  }
}
</style>
