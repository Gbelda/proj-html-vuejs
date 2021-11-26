<template>
  <div class="staff_card">
    <img :src="require(`../assets/img/${img}`)" alt="" />
    <div class="staff_data">
      <h3>{{ name }}</h3>
      <h3>{{ job }}</h3>
      <p>{{ text }}</p>
      <div class="social">
        <img src="../assets/img/facebook-logo.jpg" alt="" />
        <img src="../assets/img/twitter-logo.jpg" alt="" />
        <img src="../assets/img/instagram-logo.jpg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    img: String,
    name: String,
    job: String,
    text: String,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.staff_card {
  width: 31%;
  color: $text_gray;
  padding: 4rem 0px 6rem;

  img {
    width: 100%;
    margin-bottom: -5px;
  }

  .staff_data {
    width: 100%;
    background-color: white;
    padding: 3rem 2.5rem;
    line-height: 2.5rem;
    font-weight: 300;

    h3 {
      color: $text_primary;
      font-weight: 300;
    }

    p {
      padding-top: 2rem;
      font-size: 0.9rem;
      padding: 0px 0.3rem;
    }

    .social {
      padding-top: 2rem;
      img {
        width: 30px;
        margin-right: 0.5rem;
      }
    }
  }
}
</style>