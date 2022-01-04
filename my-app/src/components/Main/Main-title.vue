<template>
  <div class="main__title">
    <h2>
      Welcome To <br />
      My Personal Portfolio
    </h2>
    <p>
      The purpose of JavaScript Mastery is to help aspiring and established
      developers to take their development skills to the next level and build
      awesome apps.
    </p>
    <v-btn class="btn">Learn More</v-btn>
    <div class="line"></div>
  </div>
</template>

<script>
export default {
  name: "Title",
};
</script>

<style lang="scss" >
.main__title {
  h2 {
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
  p {
    max-width: 700px;
    font-size: 24px;
    line-height: 40px;
    font-weight: 300;
    padding-bottom: 1.5rem;
    color: rgba(255, 255, 255, 0.5);
  }
  .btn {
    width: 210px;
    height: 64px !important;
    border-radius: 50px;
    font-size: 20px;
    font-weight: 600;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    background: linear-gradient(270deg, #00dbd8 0%, #b133ff 100%);
    cursor: pointer;
    transition: 0.5s ease;
    position: relative;
    overflow: hidden;
    opacity: 1;
    text-transform: none !important;
    margin-bottom: 90px;
  }
  .line {
    width: 60px;
    height: 7px;
    border-radius: 50px;
    background: linear-gradient(270deg, #00dbd8 0%, #b133ff 100%);
    transition: 0.5s ease;
    margin-bottom: 80px;
  }
}
</style>
