<template>
  <footer class="d-flex justify-between">
    <div class="about_us">
      <div class="logo">
        <img src="../assets/img/medical_logo_1x_dark.png" alt="" />
      </div>
      <div class="text_container">
        <p>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium dolemue launti totam aperiam, eaque ipsa quae abillo.
          Invente veriatis et quasi architecto beatae luptatem accusantium,
          remaperiamsiat. Voluptatem accusest etsium doloremque laudaien. Lorem
          ipsum sits dolores ets unser.
        </p>
        <hr />
      </div>
      <div class="social">
        <h5>LEARN MORE ABOUT US</h5>
        <div class="social_icon">
          <img src="../assets/img/facebook-logo.jpg" alt="" />
          <img src="../assets/img/twitter-logo.jpg" alt="" />
          <img src="../assets/img/youtube-logo.jpg" alt="" />
          <img src="../assets/img/instagram-logo.jpg" alt="" />
        </div>
      </div>
    </div>
    <!-- ./ABOUT US -->

    <div class="contact_info">
      <h4>CONTACT INFORMATION</h4>
      <hr />
      <div class="address">
        <i class="fas fa-map-marker-alt icon"></i>
        <h6>121 King Street, London United Kingdom</h6>
      </div>
      <div class="phone">
        <i class="fas fa-phone icon"></i>
        <h6>1.800.458.556</h6>
      </div>
    </div>
    <!-- ./CONTACT INFO -->

    <div class="med_departments">
      <h4>MEDICAL DEPARTMENTS</h4>
      <hr />
      <ul class="index">
        <li
          v-for="department in departments"
          :key="department.name"
          class="d-flex align-center"
        >
          <div class="bullet d-flex justify-center align-center">
            <i class="fas fa-chevron-right"></i>
          </div>
          <h6>{{ department.name }}</h6>
        </li>
      </ul>
      <button>VIEW OUR DEPARTMENTS</button>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      departments: [
        {
          name: "Cardiology",
        },
        {
          name: "Pediatrics",
        },
        {
          name: "Diabetes Care",
        },
        {
          name: "Pre-natel Care",
        },
        {
          name: "Ultrasound Echocardiogram",
        },
      ],
    };
  },
};
</script>

<style lang='scss'>
@import "../assets/scss/variables.scss";

footer {
  padding: 6rem;
  /******************************************* COMMON ************************************************/
  .contact_info,
  .med_departments {
    hr {
      width: 35px;
      border: none;
      border-bottom: 2px solid $highlight_primary;
      margin-bottom: 1.5rem;
    }

    h4 {
      font-weight: 300;
      color: $text_primary;
      margin-bottom: 1.5rem;
    }
  }

  .about_us,
  .contact_info,
  .med_departments {
    width: 32%;
  }

  /***************************************** ABOUT US ************************************************/
  .about_us {
    .logo {
      img {
        width: 250px;
      }
    }
    .text_container {
      p {
        font-size: 0.8rem;
        line-height: 2rem;
        color: gray;
        margin: 1rem 0px;
      }

      hr {
        border: none;
        border-bottom: 1px solid lightgray;
      }
    }

    .social {
      h5 {
        font-weight: 300;
        color: $text_primary;
        padding-top: 0.5rem;
      }

      .social_icon {
        margin-top: 3rem;
        img {
          width: 30px;
          margin-right: 0.5rem;
        }
      }
    }
  }

  /*************************************** CONTACT INFO ********************************************/
  .contact_info {
    .icon {
      color: $highlight_primary;
      width: 16px;
    }

    h6 {
      font-weight: 300;
      display: inline-block;
      font-size: 0.9rem;
      margin-left: 1rem;
      color: gray;
    }
  }

  /*********************************** MEDICAL DEPARTMENTS ******************************************/
  .med_departments {
    li {
      margin-bottom: 0.5rem;

      .bullet {
        width: 20px;
        height: 20px;
        background-color: $highlight_primary;
        border-radius: 50%;
        margin-right: 0.5rem;

        i {
          font-size: 0.5rem;
          color: white;
        }
      }

      h6 {
        font-weight: 300;
        color: gray;
      }
    }

    button {
      width: 50%;
      height: 2.5rem;
      background-color: transparent;
      border: 1px solid gray;
      color: $text_primary;
      margin-top: 5rem;
    }
  }
}
</style>