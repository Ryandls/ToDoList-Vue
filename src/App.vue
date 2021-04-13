<template>
  <Body />
</template>

<script>
import Body from "./components/Body";
export default {
  name: "App",
  components: {
    Body,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html {
  position: aboslute;
  background-image: url("./assets/wallpaper.jpg");
  background-position: center center;
  width: 100%;
  height: 100%;
}

body {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color: black;
}

#app {
  width: 380px;
  height: 70vh;
  margin: 5vh auto;
  padding: 10px;
  background: rgb(237, 243, 243);
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  overflow: auto;
  border-radius: 15px;
}
</style>
