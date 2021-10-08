<template>
  <div id="app">
    <main>
      <navigation></navigation>
      <bulma-examples></bulma-examples>
    </main>
  </div>
</template>

<script>
import BulmaExamples from './components/BulmaExamples.vue';
import Navigation from './components/Navigation.vue';

export default {
  name: 'App',
  components: {
    Navigation,
    BulmaExamples
  }
}
</script>

<style>

</style>
