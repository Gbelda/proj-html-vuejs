<template>
  <div class="facility" :class="Id">
    <h4>{{ name }}</h4>
    <img src="../assets/img/wave-divider.png" alt="" />
    <p>
      {{ text }}
    </p>
    <button>LEARN MORE</button>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    Id: String,
    text: String,
  },
};
</script>

<style lang="scss">
.facility {
  width: calc(100% / 3);
  text-align: center;
  height: 300px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  line-height: 2.5rem;

  img {
    width: 10%;
  }

  h4 {
    font-weight: 400;
    font-size: 1rem;
    padding-bottom: 0.5rem;
  }

  p {
    font-weight: 300;
    font-size: 0.8rem;
    padding: 0px 1.5rem;
  }

  button {
    margin-top: 1rem;
    color: white;
    background: none;
    border: 2px solid white;
    height: 40px;
    width: 150px;
  }
}
</style>