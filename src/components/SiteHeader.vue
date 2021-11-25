<template>
  <header class="d-flex align-center">
    <nav class="d-flex justify-between align-center">
      <div class="logo">
        <img src="../assets/img/medical_logo_1x_light.png" alt="" />
      </div>
      <div class="nav_options d-flex align-center">
        <ul class="nav_index d-flex">
          <li
            v-for="page in pages"
            :key="page.section"
            :class="{ selected: page.selected }"
          >
            {{ page.section.toUpperCase() }}
          </li>
        </ul>
        <button>MAKE APPOINTMENT</button>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      pages: [
        {
          section: "home",
          selected: true,
        },
        {
          section: "about",
          selected: false,
        },
        {
          section: "departments",
          selected: false,
        },
        {
          section: "articles",
          selected: false,
        },
      ],
    };
  },
};
</script>

<style lang='scss'>
@import "../assets/scss/variables.scss";
header {
  background-color: transparent;
  height: 90px;
  position: absolute;
  width: 100%;

  nav {
    width: 100%;
    padding: 0px 5rem;
    font-size: 0.8rem;

    .logo {
      width: 30%;

      img {
        width: 45%;
      }
    }

    .nav_index {
      color: white;
      list-style: none;
      margin-right: 3rem;
      font-weight: 300;

      li {
        padding-left: 3rem;
      }
      .selected {
        color: $highlight_primary;
      }
    }

    button {
      padding: 0.7rem 1.8rem;
      background-color: $highlight_primary;
      color: white;
      border: none;
      border-radius: 3px;
    }
  }
}
</style>