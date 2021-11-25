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

    <section class="staff">
      <section-heading :icon="'icon-5.png'" :title="'MEET OUR DOCTORS'" />
      <div class="row d-flex justify-between">
        <staff-card
          v-for="doctor in doctors"
          :key="doctor.name"
          :img="doctor.img"
          :name="doctor.name"
          :job="doctor.job"
          :text="doctor.text"
        />
      </div>
    </section>
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SectionHeading from "./SectionHeading.vue";
import ServicesCard from "./ServicesCard.vue";
import StaffCard from "./StaffCard.vue";
export default {
  components: {
    Jumbotron,
    ServicesCard,
    SectionHeading,
    StaffCard,
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
      doctors: [
        {
          img: "doctor-1.jpg",
          name: "Jon Snow",
          job: "Anesthesiologist",
          text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
        {
          img: "doctor-2.jpg",
          name: "Tony Stark",
          job: "Cardiologist",
          text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
        {
          img: "doctor-3.jpg",
          name: "Anna Smith",
          job: "Nurse Practitioner",
          text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
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
      color: gray;
    }

    p {
      margin: auto;
      width: 70%;
      color: $text_gray;
      font-size: 1.4rem;
    }
  }
}
.staff {
  background-color: $bg_gray;

  .row {
    width: 60%;
    margin: auto;
  }
}
</style>