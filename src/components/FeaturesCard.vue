<template>
  <div class="card">
    <img :src="require(`../assets/img/${icon}`)" alt="" />
    <h3>{{ section_title.toUpperCase() }}</h3>
    <p>
      {{ section_text }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    icon: String,
    section_title: String,
    section_text: String,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.card {
  width: 24%;
  color: $text_gray;
  padding: 4rem 0px;

  h3 {
    font-weight: 300;
  }

  p {
    font-size: 0.9rem;
    padding: 0px 0.3rem;
  }
}
</style>