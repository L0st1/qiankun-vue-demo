<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <button @click="srcollToTest">测试scrollTo滚动</button>
    <button @click="srcollIntoViewTest">测试srcollIntoView滚动</button>
    <router-view/>
  </div>
</template>

<script>
export default {
  methods: {
    srcollToTest: () => {
      window.scrollTo({ top: 1000 });
    },
    srcollIntoViewTest: () => {
      //
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 3000px;
}

button {
  position: absolute;
  bottom: 10px;
}

button:nth-of-type(1) {
  margin-left: 300px;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
