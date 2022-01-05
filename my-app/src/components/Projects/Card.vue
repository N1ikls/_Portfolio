<template>
  <div color="#0f1624" class="projects__card card">
    <img class="card__img" src="@/assets/1.png" />
    <div class="card__title">{{ this.title }}</div>
    <div class="card__text">
      {{ this.text }}
    </div>
    <div class="card__stack stack">
      <div class="stack__title">Stack</div>
      <ul class="stack__items">
        <li class="stack__item" v-for="(i, index) in stack" :key="index">
          {{ i }}
        </li>
      </ul>
    </div>
    <div class="buttons">
      <v-btn v-for="(i, index) in btn" :key="index" class="btn">{{ i }}</v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      btn: ["Code", "Source"],
    };
  },
  props: ["title", "text", "stack"],
};
</script>

<style lang="scss" scoped>
.buttons {
  width: 80%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}
.stack__item {
  width: 80%;
  margin: 0 auto;
  color: #d4c0c0;
  font-style: 2rem;
  line-height: 24px;
  text-align: justify;
}
.stack__items {
  display: flex;
  align-items: center;
}
.card__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  overflow: hidden;
}
.projects__card {
  box-shadow: 3px 3px 20px rgba(80, 78, 78, 0.5) !important;
  text-align: center;
  border-radius: 10px;
  width: 310px;
}
.stack__title {
  width: 80%;
  margin: 0 auto;
  color: #e4e6e7;
  font-style: 2rem;
  line-height: 24px;
  text-align: center;
  padding: 15px;
}
.card__title {
  font-weight: 500;
  letter-spacing: 2px;
  color: #9cc9e3;
  padding: 0.5rem 0;
  font-size: 2rem;
  &::after {
    content: "";
    display: block;
    width: 50px;
    height: 3px;
    margin: 20px auto;
    border: 0;
    background: #d0bb57;
  }
}
.card__text {
  width: 80%;
  margin: 0 auto;
  color: #e4e6e7;
  font-style: 2rem;
  line-height: 24px;
  text-align: justify;
}
.card__stack {
  margin-bottom: 50px;
}
.btn {
  border-radius: 50px;
  font-size: 14px;
  font-weight: 400;
  color: #fff;
  background: linear-gradient(270deg, #00dbd8 0%, #b133ff 100%);
  cursor: pointer;
  transition: 0.5s ease;
  position: relative;
  overflow: hidden;
  opacity: 1;
  text-transform: none !important;
  margin-bottom: 20px;
}

@media (max-width:442px) {
  .projects__card {
    max-width: 270px;
  }
  
}
</style>
