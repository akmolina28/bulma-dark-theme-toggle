<template>
  <div id="app">
    <main>
      <navigation></navigation>

      <section class="hero is-primary">
        <div class="hero-body has-text-centered">
          <p class="title">bulma-dark-theme-toggle</p>
          <p>
            Toggle the theme with the <i class="fas fa-sun"></i>/<i
              class="fas fa-moon"
            ></i>
            icon in the navbar.
          </p>
          <div class="p-2">
            <a href="https://github.com/akmolina28/bulma-dark-theme-toggle/" class="button mr-2">
              <span class="icon">
                <i class="fab fa-github"></i>
              </span>
              <span>GitHub</span>
            </a>
            <a href="https://www.buymeacoffee.com/akmolina28" rel="nofollow"
              ><img
                src="https://camo.githubusercontent.com/28aae05a0fba45679e8e27d90609601e249b64a5fe30dfef05495de4f4e318d4/68747470733a2f2f63646e2e6275796d6561636f666665652e636f6d2f627574746f6e732f76322f64656661756c742d79656c6c6f772e706e67"
                alt="Buy Me A Coffee"
                style="height: 37px; width: 130px; max-width: 100%; margin-top:1px"
                data-canonical-src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png"
            /></a>
          </div>
        </div>
      </section>

      <bulma-examples></bulma-examples>
    </main>
  </div>
</template>

<script>
import BulmaExamples from "./components/BulmaExamples.vue";
import Navigation from "./components/Navigation.vue";

export default {
  name: "App",
  components: {
    Navigation,
    BulmaExamples,
  },
};
</script>

<style>
</style>
