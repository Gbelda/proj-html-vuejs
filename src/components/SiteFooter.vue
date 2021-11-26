<template>
  <footer class="d-flex">
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
  </footer>
</template>

<script>
export default {};
</script>

<style lang='scss'>
@import "../assets/scss/variables.scss";

footer {
  padding: 6rem;

  .about_us {
    width: 32%;
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

  .contact_info {
    width: 32%;

    h4 {
      font-weight: 400;
      color: $text_primary;
      margin-bottom: 1.5rem;
    }

    hr {
      width: 35px;
      border: none;
      border-bottom: 2px solid $highlight_primary;
      margin-bottom: 1.5rem;
    }

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
}
</style>