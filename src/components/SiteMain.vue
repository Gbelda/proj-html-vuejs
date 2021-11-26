<template>
  <main>
    <jumbotron />
    <!-- ./JUMBOTRON -->

    <section class="features text-center">
      <div class="section_head">
        <h2>Welcome to Avada Health</h2>
        <p>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae
          ab illo
        </p>
      </div>
      <div class="row d-flex justify-between">
        <features-card
          v-for="feature in features"
          :key="feature.icon"
          :section_text="feature.text"
          :section_title="feature.title"
          :icon="feature.icon"
        />
      </div>
    </section>
    <!-- ./HOSPITAL FEATURES SECTION -->

    <section class="staff">
      <section-heading
        :icon="'icon-5.png'"
        :title="'MEET OUR DOCTORS'"
        :withIcon="true"
      />
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
    <!-- ./STAFF DOCTORS SECTION -->

    <section class="services">
      <section-heading
        :icon="'icon-6.png'"
        :title="'OUR HEALTH SERVICES'"
        :withIcon="true"
      />
      <div class="row d-flex justify-between flex-wrap">
        <features-card
          v-for="service in services"
          :key="service.icon"
          :section_text="service.text"
          :section_title="service.title"
          :icon="service.icon"
        />
      </div>
    </section>
    <!-- ./SERVICES SECTION -->

    <section class="facilities">
      <div class="facilities_header d-flex flex-column align-center">
        <section-heading
          :icon="'icon-7.png'"
          :title="'TOUR OUR FACILITIES'"
          :withIcon="true"
        />
        <div class="play_container">
          <img src="../assets/img/play-icon.png" alt="" id="play-icon" />
        </div>
      </div>
      <!-- ./FACILITIES HEADER -->

      <div class="departments d-flex">
        <department-card
          v-for="department in departments"
          :key="department.name"
          :Id="department.class"
          :name="department.name"
          :text="department.text"
        />
      </div>
      <!-- ./DEPARTMENTS -->
    </section>
    <!--./FACILITIES -->

    <section class="appointment">
      <div class="container">
        <section-heading :withIcon="false" :title="'Make An Appointment'" />
      </div>
      <appointment-form />
    </section>
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SectionHeading from "./SectionHeading.vue";
import FeaturesCard from "./FeaturesCard.vue";
import StaffCard from "./StaffCard.vue";
import DepartmentCard from "./DepartmentCard.vue";
import AppointmentForm from "./AppointmentForm.vue";
export default {
  components: {
    Jumbotron,
    SectionHeading,
    StaffCard,
    FeaturesCard,
    DepartmentCard,
    AppointmentForm,
  },
  data() {
    return {
      features: [
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
      services: [
        {
          icon: "icon-14.png",
          title: "rehabilitation center",
          text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas",
        },
        {
          icon: "icon-15.png",
          title: "dental implants",
          text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas",
        },
        {
          icon: "icon-16.png",
          title: "medicine research",
          text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas",
        },
        {
          icon: "icon-11.png",
          title: "blood bank",
          text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas",
        },
        {
          icon: "icon-12.png",
          title: "pharmaceutical advice",
          text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas",
        },
        {
          icon: "icon-13.png",
          title: "medical counseling",
          text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas",
        },
      ],
      departments: [
        {
          name: "Emergency Care",
          text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque",
          class: "emergency_care",
        },
        {
          name: "Expert Diagnostics",
          text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque",
          class: "diagnostics",
        },
        {
          name: "Superb Rehabilitation",
          text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque",
          class: "rehab",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
/*********************************** FEATURES ***********************************/
.features {
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

/************************************* STAFF ***********************************/
.staff {
  background-color: $bg_gray;

  .row {
    width: 60%;
    margin: auto;
  }
}

/*********************************** SERVICES **********************************/
.services {
  .row {
    width: 60%;
    margin: auto;

    .card {
      width: 32%;
      text-align: center;
      line-height: 2.5rem;
    }
  }
}

/*********************************** FACILITIES ********************************/
.facilities {
  .facilities_header {
    background-image: url(../assets/img/tour-facilities.jpg);
    background-size: cover;
    height: 700px;
    background-position-y: center;
  }

  h2,
  h4,
  p {
    color: white;
  }

  .play_container {
    padding-bottom: 9rem;
  }

  .departments {
    .emergency_care {
      background-color: #3aafbf;
    }

    .diagnostics {
      background-color: #3597c3;
    }

    .rehab {
      background-color: #327ec7;
    }
  }
}

/********************************** APPOINTMENT ********************************/
.appointment {
  background-image: url(../assets/img/appointment.jpg);
  background-position: center;

  h2,
  p {
    color: white;
  }
}
</style>