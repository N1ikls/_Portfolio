<template>
  <header class="header">
    <div class="header__container _container">
      <div class="header__row">
        <div class="header__title text-center">
          <v-btn class="icon" color="white" href="https://ru.vuejs.org/" icon>
            <v-icon>mdi-vuejs</v-icon>
          </v-btn>
          Portfolio
        </div>

        <nav class="header__menu menu">
          <ul class="menu__list">
            <li v-for="(item, index) in list" :key="index" class="menu__item">
              {{ item }}
            </li>
          </ul>
        </nav>
      </div>
      <div class="header__icons text-center">
        <v-btn
          class="icon"
          color="white"
          icon
          v-for="(icon, index) in icons"
          :key="index"
          :href="icon.link"
        >
          <v-icon>{{ icon.icon }}</v-icon>
        </v-btn>
      </div>
    </div>
  </header>
</template>

<script>
//import { Slide } from "vue-burger-menu";
export default {
  data: () => {
    return {
      title: "Portfolio",
      list: ["Projects", "Technologies", "About"],
      icons: [
        { icon: "mdi-github", link: "https://github.com/N1ikls" },
        { icon: "mdi-instagram", link: "https://www.instagram.com/n1kolaayy/" },
        { icon: "mdi-account-circle", link: "https://vk.com/id505833989" },
      ],
    };
  },
  components: {
   // Slide,
  },
};
</script>

<style lang="scss" scoped>
.header__row {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}
.header__container {
  display: flex;
  min-height: 70px;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}

.header__title {
  color: white;
  font-size: 18px;
  margin-right: 110px;
}
.menu__item {
  color: rgba(255, 255, 255, 0.75);
  font-size: 20px;
  &:hover {
    color: #fff;
    opacity: 1;
    cursor: pointer;
  }
  &:not(:last-child) {
    margin-right: 70px;
  }
}
.menu__list {
  display: flex;
  align-items: center;
}
.icon {
  &:not(:last-child) {
    margin-right: 30px;
  }
}
@media (max-width:829px) {
  .header__title {
    padding-left: 30%;
  }
  .menu__list {
    padding: 1.7rem;
    flex-wrap: wrap;
  }
  .menu__item {
    font-size: 30px;
    padding: 1rem;
  }
  .header__row {
   
  }
  .header__conatiner {
    justify-content: center !important;
  }
  .header__icons {
    padding-left: 30%;
  }
}
</style>
