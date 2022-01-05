<template>
  <div class="main__technologies technologies">
    <Gradient_line class="mb-3 mt-8" />
    <Title :title="title" />
    <Text_body :text="text" />
    <div class="list__row">
      <div class="technologies__list list">
        <v-btn icon color="white">
          <v-icon>mdi-react</v-icon>
        </v-btn>
        <div class="list__title">Front-End</div>
        <div class="list__text">
          Experiece with <br />
          React.js
        </div>
      </div>
      <div class="technologies__list list">
        <v-btn icon color="white">
          <v-icon>mdi-database</v-icon>
        </v-btn>
        <div class="list__title">Back-end</div>
        <div class="list__text">
          Experiece with <br />
          Node and DataBase
        </div>
      </div>
      <div class="technologies__list list">
        <v-btn icon color="white">
          <v-icon>mdi-vuejs</v-icon>
        </v-btn>
        <div class="list__title">Front-End</div>
        <div class="list__text">
          Experiece with <br />
          Vue.js and Vuetify
        </div>
      </div>
    </div>
    <Gradient_line class="mb-3 mt-0" />
  </div>
</template>

<script>
import Text_body from "@/Global/Components/Text";
import Gradient_line from "@/Global/Components/Gradient_line.vue";
import Title from "@/Global/Components/Title.vue";
export default {
  data: () => {
    return {
      title: "Technologies",
      text: "   I've worked with a range a technologies in the web development world. From Back-end To Design",
    };
  },
  components: {
    Gradient_line,
    Title,
    Text_body,
  },
};
</script>

<style lang="scss" scoped>
.technologies__list {
  flex: 0 1 33.333%;
}
.list__row {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  padding-bottom: 50px;
  padding-top: 20px;
}
.list__title {
  font-weight: 700;
  font-size: 28px;
  line-height: 32px;
  letter-spacing: 0.02em;
  color: #ffffff;
  margin-bottom: 8px;
}
.list__text {
  font-size: 18px;
  line-height: 30px;
  color: rgba(255, 255, 255, 0.75);
}
// @media (max-width: 500px) {
//   .technologies__list {
//     flex: 0 1 100%;
//   }
// }
</style>
