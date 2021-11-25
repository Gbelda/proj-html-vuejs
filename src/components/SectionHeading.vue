<template>
  <div class="section_header">
    <img :src="require(`../assets/img/${icon}`)" alt="" />
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

  h2 {
    padding-bottom: 2.5rem;
    font-weight: 300;
    color: gray;
    font-size: 2.5rem;
  }

  hr {
    width: 20%;
    margin: auto;
  }

  p {
    margin: auto;
    width: 60%;
    color: $text_gray;
    font-size: 1.2rem;
    font-weight: 300;
    line-height: 3rem;
    padding-top: 2rem;
  }
}
</style>