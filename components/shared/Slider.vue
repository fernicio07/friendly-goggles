<template>
  <div>
    <transition-group tag="div">
      <div v-for="i in [currentIndex]" :key="i">
        <img :src="require(`../../assets/img/slideshow/${currentImg}.jpg`)" />
      </div>
    </transition-group>
  </div>
</template>

<script>
export default {
  name: 'Slider',
  data() {
    return {
      images: ['1', '2', '3'],
      timer: null,
      currentIndex: 0,
    }
  },

  computed: {
    currentImg() {
      return this.images[Math.abs(this.currentIndex) % this.images.length]
    },
  },

  mounted() {
    this.startSlide()
  },

  methods: {
    startSlide() {
      this.timer = setInterval(this.next, 4000)
    },

    next() {
      this.currentIndex += 1
    },
    prev() {
      this.currentIndex -= 1
    },
  },
}
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.9s ease;
  overflow: hidden;
  visibility: visible;
  position: absolute;
  width: 100%;
  opacity: 1;
}

.fade-enter,
.fade-leave-to {
  visibility: hidden;
  width: 100%;
  opacity: 0;
}

img {
  border: 4px solid #fff;
  box-shadow: rgb(0 0 0 / 50%) 4px 4px 5px;
  margin-bottom: 2rem;
  width: 100%;
}

@media screen and (max-width: 375px) {
  .main-content {
    grid-template-columns: auto;
  }
}
</style>
