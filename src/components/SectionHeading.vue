<template>
  <div class="section_header">
    <img :src="require(`../assets/img/${icon}`)" alt="" v-if="withIcon" />
    <h2>{{ title }}</h2>
    <hr />
    <p>
      Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium
      doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo
      inventore veritatis et quasi architecto beatae
    </p>
  </div>
</template>

<script>
export default {
  props: {
    icon: String,
    title: String,
    withIcon: Boolean,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.section_header {
  text-align: center;
  width: 60%;
  margin: auto;
  padding-top: 5rem;

  img {
    filter: hue-rotate(50deg);
  }

  h2 {
    padding-bottom: 2.5rem;
    font-weight: 300;
    font-size: 2.2rem;
    color: $text_primary;
  }

  hr {
    width: 20%;
    margin: auto;
  }

  p {
    margin: auto;
    width: 59%;
    color: $text_primary;
    font-size: 1.2rem;
    font-weight: 300;
    line-height: 3rem;
    padding-top: 2rem;
  }
}
</style>