<template>
  <div class="card staff_card">
    <img :src="require(`../assets/img/${img}`)" alt="" />
    <div class="staff_data">
      <h3>{{ name }}</h3>
      <h3>{{ job }}</h3>
      <p>{{ text }}</p>
      <div class="social"></div>
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
    }

    p {
      padding-top: 2rem;
    }
  }
}
</style>