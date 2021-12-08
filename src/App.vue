<template>
  <header class="header"></header>
  <router-view/>
  <footer class="footer"></footer>
</template>

<style lang="scss">
body {
  margin: 0;
  background: #b9e796;
  background: linear-gradient(137deg, #b9e796 0%, #ffa541 100%);
  font: 400 14px/1.4 #2c3e50;
	scroll-behavior: smooth;
	min-width: 320px;
	overflow-y: scroll;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

header {
  height: 60px;
  background: #ffffff;
}

footer {
  height: 160px;
  background: #2c3e50;
  color: #ffffff;
}
</style>
