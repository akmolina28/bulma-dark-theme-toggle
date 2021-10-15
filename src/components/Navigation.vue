<template>
  <nav class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
    <section class="container">
      <div class="navbar-brand">
        <a class="navbar-item" href="https://bulma.io">
          <img
            src="https://bulma.io/images/bulma-logo.png"
            width="112"
            height="28"
          />
        </a>

        <a
          role="button"
          class="navbar-burger pl-4 pt-3"
          aria-label="menu"
          aria-expanded="false"
          data-target="navbarBasicExample"
          @click="toggleDarkMode"
        >
          <transition name='rotate' mode="out-in">
            <i v-if="darkMode" :key="1" class="fas fa-moon"></i>
            <i v-if="!darkMode" :key="0" class="fas fa-sun"></i>
          </transition>
        </a>
      </div>

      <div class="navbar-menu">
        <div class="navbar-start">
          <a class="navbar-item"> Home </a>

          <a class="navbar-item"> Documentation </a>

          <div class="navbar-item has-dropdown is-hoverable">
            <a class="navbar-link"> More </a>

            <div class="navbar-dropdown">
              <a class="navbar-item"> About </a>
              <a class="navbar-item"> Jobs </a>
              <a class="navbar-item"> Contact </a>
              <hr class="navbar-divider" />
              <a class="navbar-item"> Report an issue </a>
            </div>
          </div>
        </div>
        
        <div class="navbar-end">
          <div class="navbar-item">
            <a @click="toggleDarkMode">
              <transition name='rotate' mode="out-in">
                <i v-if="darkMode" :key="1" class="fas fa-moon"></i>
                <i v-if="!darkMode" :key="0" class="fas fa-sun"></i>
              </transition>
            </a>
          </div>
        </div>
      </div>
    </section>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      menuActive: false,
      darkMode: false,
    };
  },
  mounted() {
    if (localStorage.darkMode) {
      this.darkMode = localStorage.darkMode === 'true';
      this.updateRoot();
    }
  },
  watch: {
    darkMode(newValue) {
      localStorage.darkMode = newValue;
    },
  },
  methods: {
    toggleDarkMode() {
      this.darkMode = !this.darkMode;
      this.updateRoot();
    },
    updateRoot() {
      const root = document.getElementsByTagName('html')[0];
      root.className = this.darkMode ? 'dark-theme' : 'light-theme';
    },
  },
};
</script>

<style lang="scss">
@keyframes rotateOut {
    0% { opacity: 0; transform: scale(0) rotate(180deg); }
    100% { opacity: 1; transform: scale(1) rotate(0deg); }
}

@keyframes rotateIn {
    0% { opacity: 0; transform: scale(0) rotate(-180deg); }
    100% { opacity: 1; transform: scale(1) rotate(0deg); }
}

.rotate-enter-active {
    animation: rotateIn .2s;
}

.rotate-leave-active {
    animation: rotateOut .2s reverse;
}
</style>