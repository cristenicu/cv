<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div> -->
  <router-view/>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Barlow:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

body {
  margin: unset;
}

#app {
  font-family: 'Barlow', sans-serif;
}

h1, h2, h3, h4, p {
  margin: unset;
}

h1 {
  font-size: 60px;
  font-weight: 900;

  @include media($from: "lg") {
    font-size: 100px;
  }
}

h2 {
  font-size: 60px;
  font-weight: 600;

  @include media($from: "lg") {
    font-size: 100px;
  }
}

h3 {
  font-size: 30px;
  font-weight: 900;

  @include media($from: "lg") {
    font-size: 50px;
  }
}

h4 {
  font-size: 24px;
  font-weight: 900;

  @include media($from: "lg") {
    font-size: 42px;
  }
}

a {
  color: white;
}

p {
  font-size: 24px;
  font-weight: 600;
  color: #ACACAF;
}
</style>
