<template>
  <main>
    <section class="jumbotron">
      <div class="jumbo_txt">
        <h1>
          Caring
          <span class="highlight">For Life</span>
        </h1>
        <p>
          Kind words can be short and easy to speak, but their echoes are truly
          endless. Avada Health focuses on you as if it was our own family.
        </p>
        <button>LEARN MORE</button>
      </div>
    </section>
  </main>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.jumbotron {
  min-height: 100vh;
  background-image: url(../assets/img/header-image-homepage.jpg);
  background-size: 113%;
  background-position-x: center;

  .jumbo_txt {
    width: 55%;
    padding-top: 19rem;
    margin: auto;
    color: white;

    h1 {
      font-weight: 300;
      font-size: 4rem;

      .highlight {
        color: $highlight_primary;
      }
    }
    p {
      font-weight: 300;
      font-size: 1.2rem;
      width: 60%;
      padding: 2.2rem 0px;
    }

    button {
      font-size: 1rem;
      padding: 0.9rem 2.5rem;
      background-color: $highlight_primary;
      color: white;
      border: none;
      border-radius: 3px;
    }
  }
}
</style>