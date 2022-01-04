<template>
  <v-app>
    <div id="app">
      <Animation></Animation>
      <router-view />
    </div>
  </v-app>
</template>
<script>
import Animation from "./Animation/BackAnimation";
export default {
  components: {
    Animation,
  },
};
</script>
<style lang="scss">
.backanimation {
  position: absolute;
  top: 5%;
  left: 40%;
  right: 0%;
  width: 800px;
  height:500px;
}
body {
  font-family: "Space Grotesk", sans-serif;
}
@import url("https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;700&display=swap");

*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  border: 0;
  box-sizing: border-box;
}
ul[class],
ol[class] {
  padding: 0;
}
body,
h1,
h2,
h3,
h4,
p,
ul[class],
ol[class],
li,
figure,
figcaption,
blockquote,
dl,
dd {
  margin: 0;
}
/* Выставляем основные настройки по-умолчанию для body */
body {
  min-height: 100vh;
  scroll-behavior: smooth;
  text-rendering: optimizeSpeed;
  line-height: 1.5;
  font-style: normal;
}
//hsl(204, 23.8%, 95.9%)
//hsl(232.7, 27.3%, 23.7%)
ul[class],
ol[class] {
  list-style: none;
}
#app {
  min-height: 100%;
  overflow: hidden;
  background: #0f1624;
  position: relative;
}
._container {
  max-width: 1040px;
  margin: 0 auto;
  padding: 0 15px;
  box-sizing: content-box;
  grid-template-columns: 1fr 1fr;
}
</style>
