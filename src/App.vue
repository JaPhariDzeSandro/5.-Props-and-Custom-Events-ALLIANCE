<template>
  <ActiveUser-tag
    v-bind:uname="user.name"
    v-bind:uage="user.age"
  ></ActiveUser-tag>
  <UserData-tag v-on:changeableName="nameChanged" v-on:changeableAge="ageChanged"></UserData-tag>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: "Sandro",
        age: "20",
      },
    };
  },
  methods: {
    nameChanged(name) {
      this.user.name = name;
    },
    ageChanged(age) {
      this.user.age = age;
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: "Jost", sans-serif;
  background: #240035;
}

body {
  margin: 0;
}

header {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem auto;
  border-radius: 10px;
  border: 2px solid black;
  padding: 1rem;
  background-color: #58004d;
  color: rgb(255, 255, 255);
  text-align: center;
  width: 90%;
  max-width: 40rem;
}

input {
  display: block;
  margin: 10px auto;
  border-radius: 20px;
  border: 0;
  min-height: 50px;
  width: 20%;
  box-shadow: 1px 1px 8px #000000;
  background-color: #58004d;
  color: rgb(255, 255, 255);
  padding: 10px;
}
::placeholder {
  color: #ffffff;
  padding: 10px;
  font-weight: bold;
}
</style>
