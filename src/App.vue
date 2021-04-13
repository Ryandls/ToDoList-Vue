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
  background-color: rgb(53, 227, 240);
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color:rgb(233, 36, 128);
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
  border-radius: 10px;
}
h1 {
  text-align: center;
}

form {
  width: 100%;
  display: flex;
  border-radius: 3px;
}

form input {
  width: 80%;
  border: 0;
  padding: 10px;
  border-top-left-radius: 3px;
  border-bottom-left-radius: 3px;
}

form button {
  width: 20%;
  border: 0;
  background-color: rgb(233, 36, 128);
  color: white;
  padding: 10px;
  border-top-right-radius: 3px;
  border-bottom-right-radius: 3px;
}
</style>
