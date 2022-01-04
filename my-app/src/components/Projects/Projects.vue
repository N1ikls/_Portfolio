<template>
  <div class="main__projects projects">
    <div class="projects__title main__title">
      <h2>Projects</h2>
    </div>
    <div class="projects__row">
      <Card
        v-for="(card, index) in cards"
        :key="index"
        :title="card.title"
        :text="card.text"
        :stack="card.stack"
      />
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  data: () => {
    return {
      cards: [
        {
          title: "Patreon",
          text: " Using React, Node.js, Express & MongoDB you ll learn how to build a Full Stack MERN Application - from start to finish. The App is called Memories and it is a simple social media app that allows users to post interesting events that happened in their lives.",
          stack: ["HTML", "CSS", "JavaScript"],
        },
        {
          title: "Patreon",
          text: " Using React, Node.js, Express & MongoDB you ll learn how to build a Full Stack MERN Application - from start to finish. The App is called Memories and it is a simple social media app that allows users to post interesting events that happened in their lives.",

          stack: ["HTML", "CSS", "JavaScript"],
        },
        {
          title: "Patreon",
          text: " Using React, Node.js, Express & MongoDB you ll learn how to build a Full Stack MERN Application - from start to finish. The App is called Memories and it is a simple social media app that allows users to post interesting events that happened in their lives.",
          stack: ["HTML", "CSS", "JavaScript"],
        },
        {
          title: "Patreon",
          text: " Using React, Node.js, Express & MongoDB you ll learn how to build a Full Stack MERN Application - from start to finish. The App is called Memories and it is a simple social media app that allows users to post interesting events that happened in their lives.",
          stack: ["HTML", "CSS", "JavaScript"],
        },
      ],
    };
  },
  components: {
    Card,
  },
};
</script>

<style lang="scss" scoped>
.projects__row {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(310px, 1fr));
  place-items: center;
  column-gap: 3.5rem;
  row-gap: 3.5rem;
  padding: 3.5rem;
}
</style>
