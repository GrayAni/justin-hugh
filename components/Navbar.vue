<template>
  <div class="navbar">
    <nav>
      <div class="navbar__logo">
        <p>jh</p>
      </div>
      <div class="navbar__menu">
        <ul>
          <li>
            <!-- <input type="text" placeholder="Enter collection" /> -->
          </li>
          <li>Search</li>
          <li>Collections</li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  mounted() {
    this.slider()
  },
  methods: {
    slider() {
      gsap.from('.navbar', { opacity: 0, duration: 0.5, y: -50 })
    },
  },
}
</script>
<style lang="scss" scoped>
.navbar {
  width: 85%;
  margin: 0 auto;
  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 15px 0px;
  }
  &__logo {
    p {
      font-weight: bold;
      font-size: 24px;
      font-family: 'Playfair Display', serif;
    }
  }
  &__menu {
    ul {
      display: flex;
      align-items: center;
      list-style: none;
    }
    li {
      font-size: 12px;
      margin-left: 40px;
      text-transform: uppercase;
      font-weight: 600;
      letter-spacing: 1.7px;
    }
  }
}
</style>
