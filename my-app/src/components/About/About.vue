<template>
  <div class="main__about about">
    <Title :title="title"></Title>
    <Text_body :text="text"></Text_body>
  </div>
</template>

<script>
import Title from "../../Global/Components/Title.vue";
import Text_body from "../../Global/Components/Text.vue";
export default {
  data: () => {
    return {
      title: "About Me",
      text: " The purpose of JavaScript Mastery is to help aspiring and established developers to take their development skills to the next level and build awesome apps.",
    };
  },
  components: {
    Title,
    Text_body
  },
};
</script>

<style></style>
