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
body {
  background-color: rgb(25, 97, 230);
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color:black;
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
