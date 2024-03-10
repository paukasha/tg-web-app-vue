<template>
  <div id="app">
    <button @click="onClose">Close</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
    tg: ''
  },
  mounted() {
    this.tg = window.Telegram.WebApp
    this.tg.ready()
  },
  methods: {
    onClose() {
      this.tg.close()
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
