<template>
  <div id="app">
    <button @click="onClose">Close</button>
  </div>
</template>

<script>
const tg = window.Telegram.WebApp
export default {
  name: 'App',
  components: {},
  mounted() {
    tg.ready()
  },
  methods: {
    onClose() {
      tg.close()
    }
  }
}
</script>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: var(--tg-theme-bg-color);
  color: var(--tg-theme-text-color);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
