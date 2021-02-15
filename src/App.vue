<template>
    <Nav />
    <Chat />
</template>

<script>
import Nav from "./components/Nav";
import Chat from "./components/Chat";
export default {
  name: "App",
  components: {
    Nav,
    Chat,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
