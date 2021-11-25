<template>
  <main>
    <jumbotron />
    <!-- ./Jumbotron -->

    <section class="services text-center">
      <div class="section_head">
        <h2>Welcome to Avada Health</h2>
        <p>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae
          ab illo
        </p>
      </div>
      <div class="row d-flex justify-between">
        <services-card
          v-for="service in services"
          :key="service.icon"
          :section_text="service.text"
          :section_title="service.title"
          :icon="service.icon"
        />
      </div>
    </section>
    <!-- ./Services Section -->

    <section class="staff"></section>
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import ServicesCard from "./ServicesCard.vue";
export default {
  components: {
    Jumbotron,
    ServicesCard,
  },
  data() {
    return {
      services: [
        {
          icon: "icon-1.png",
          title: "same day appointments",
          text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium",
        },
        {
          icon: "icon-2.png",
          title: "world class facilities",
          text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium",
        },
        {
          icon: "icon-3.png",
          title: "expert doctors",
          text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium",
        },
        {
          icon: "icon-4.png",
          title: "complementary therapies",
          text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.services {
  width: 60%;
  margin: auto;
  font-weight: 300;
  line-height: 2rem;
  margin-top: 5rem;
  line-height: 2.5rem;

  .section_head {
    h2 {
      color: $text_primary;
      font-weight: 300;
      padding-bottom: 1rem;
      font-size: 2.5rem;
    }

    p {
      margin: auto;
      width: 70%;
      color: $text_gray;
      font-size: 1.4rem;
    }
  }
}
</style>