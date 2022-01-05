<template>
  <footer class="footer">
    <div class="footer__container _container">
      <Gradient_line class="mb-8 mt-0" />
      <ul class="footer__list list">
        <div class="list__item">
          <h4>Call</h4>
          <p>+7 918 277 39 34</p>
        </div>
        <div class="list__item">
          <h4>Email</h4>
          <p>sau3000@mail.ru</p>
        </div>
      </ul>
      <div class="footer__bottom">
        <div class="footer__text">
          <p>Innovating one project at a time</p>
        </div>
        <div class="footer__icons text-center">
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
    </div>
  </footer>
</template>

<script>
import Gradient_line from "@/Global/Components/Gradient_line.vue";
export default {
  components: {
    Gradient_line,
  },
  data: () => {
    return {
      icons: [
        { icon: "mdi-github", link: "https://github.com/N1ikls" },
        { icon: "mdi-instagram", link: "https://www.instagram.com/n1kolaayy/" },
        { icon: "mdi-account-circle", link: "https://vk.com/id505833989" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.footer__container {
  width: calc(100vw - 96px);
  max-width: 800px;
  padding: 2rem 45px 15px;
  margin: 0 auto;
  box-sizing: content-box;
}
.footer__list {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  display: grid;
  grid-template-columns: repeat(3, minmax(85px, 220px));
  gap: 40px;
  padding: 40px 0px 28px;
  h4 {
    font-family: "Space Grotesk", sans-serif;
    font-style: normal;
    font-weight: 600;
    font-size: 10px !important;
    line-height: 24px;
    text-transform: uppercase;
    color: rgba(255, 255, 255, 0.4);
    margin-bottom: 16px;
  }
  p {
    font-family: "Space Grotesk", sans-serif;
    font-size: 14px !important;
    line-height: 30px;
    color: rgba(255, 255, 255, 0.75);
    margin-bottom: 16px;
    transition: all 0.3s ease 0s;
    position: relative;
    left: 0px;
    cursor: pointer;
    &:hover {
      color: #fff;
      left: 6px;
    }
  }
}
.footer__icons {
  display: flex;
  -webkit-box-align: center;
  align-items: center;
}
.footer__bottom {
  max-width: 1040px;
  display: flex;
  -webkit-box-pack: justify;
  justify-content: space-between;
  flex-wrap: wrap;
}
.footer__text {
  display: flex;
  -webkit-box-align: baseline;
  align-items: baseline;
  flex-wrap: wrap;
  margin-right: auto;
  p {
    color: rgba(255, 255, 255, 0.5) !important;
    min-width: 280px !important;
    letter-spacing: 0.02em;
    font-size: 14px;
    line-height: 30px;
    padding: 1rem;
  }
}
</style>
