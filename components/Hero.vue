<template>
  <div class="hero">
    <div class="hero__text">
      <h1 class="hero__name"><span class="hidden">justin hugh</span></h1>
      <div class="hero__other-text">
        <h3>styles and samples <span>2022</span></h3>
        <p class="hero__desc">
          <span class="hidden">
            You asked for it. We dreamt, drille, designed and lived it. Here are
            the best of our 2022 styles and samples. Let us set you apart every
            day, every where.
          </span>
        </p>
      </div>
    </div>
    <div class="hero__foot-text">
      <p>special release</p>
    </div>
    <div class="hero__images">
      <div class="image"></div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HeroComp',
  mounted() {
    this.textTransition()
  },
  methods: {
    textTransition() {
      gsap.from('.hero__name .hidden', {
        duration: 0.6,
        y: '100%',
      })
      gsap.from('.hero__other-text h3', {
        duration: 0.5,
        opacity: 0,
        x: -10000,
      })
      gsap.from('.hero__desc .hidden', {
        duration: 0.5,
        y: '100%',
        ease: 'circ',
      })

      gsap.from('.image', {
        duration: 0.5,
        x: 400,
      })
    },
  },
  computed: {},
}
</script>
<style lang="scss" scoped>
.hero {
  margin: 10vh auto 0;
  &__text {
    position: absolute;
    top: 300px;
    z-index: 2;
    transform: rotate(-90deg);

    h3 {
      font-size: 1.5rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      font-weight: 600;
      color: #545e63;
      span {
        color: #a30b37;
      }
    }
  }
  &__name {
    font-size: 6rem;
    text-transform: uppercase;
    font-weight: 900;
    position: relative;
    height: 140px;
    width: 700px;
    overflow: hidden;
    .hidden {
      position: absolute;
    }
  }
  &__desc {
    font-size: 14px;
    width: 335px;
    text-align: justify;
    line-height: 1.7;
    margin-top: 5px;
    position: relative;
    height: 140px;
    overflow: hidden;
    .hidden {
      position: absolute;
    }
  }
  &__foot-text {
    position: absolute;
    bottom: 120px;
    top: 50vh;
    right: 20px;
    z-index: 2;

    p {
      font-weight: 700;
      font-size: 12px;
      text-transform: uppercase;
      transform: rotate(90deg);
      letter-spacing: 5px;
    }
  }
  &__images {
    z-index: 1;
    position: absolute;
    right: 5%;
    top: -20vh;
    .image {
      background: url(../images/jh.png) no-repeat;
      height: 120vh;
      width: 700px;
      background-size: contain;
      transition: 0.5s;
    }
  }
}
</style>
