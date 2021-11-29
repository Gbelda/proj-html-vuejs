<template>
  <div class="play_container">
    <img
      src="../assets/img/play-icon.png"
      alt=""
      id="play-icon"
      @click="playVideo()"
    />
    <div class="video" v-if="this.showVideo">
      <video src="../assets/video/virtualtour.mp4" controls="true"></video>
      <i class="fas fa-times close" @click="hideVideo()"></i>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showVideo: false,
    };
  },
  methods: {
    playVideo() {
      this.showVideo = true;
    },
    hideVideo() {
      this.showVideo = false;
    },
  },
};
</script>

<style lang="scss">
.play_container {
  padding-bottom: 9rem;

  img {
    filter: hue-rotate(50deg);
    transition: transform 500ms ease;

    &:hover {
      cursor: pointer;
      transform: scale(1.1);
    }
  }

  .video {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 100;
    background-color: rgba(0, 0, 0, 0.705);
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;

    .close {
      font-size: 3rem;
      top: 7%;
      right: 10%;
      color: white;
      position: absolute;
      z-index: 200;

      &:hover {
        cursor: pointer;
      }
    }
  }
}
</style>