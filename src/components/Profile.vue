<template>
  <div class="profile">
    <img class="profile-image" src="/profile.jpeg" alt="">
    <div class="image-border"></div>
    <h1>Nicu</h1>
    <h2>Criste</h2>
    <div class="info">
      <div class="location">
        <i class="uil uil-map-marker-alt" />&nbsp;Cluj
      </div>
      <div class="date-of-birth">
        <i class="uil uil-calendar-alt" />&nbsp;11/03/1987
      </div>
    </div>
    <h3>ABOUT OR FUN FACTS</h3>
    <p>Continuously self-improving, curious about new technologies,
      how to make things simpler,
      better and prettier.
      Always expecting to see the materialization of those curiosities into an end product,
      the better solution.</p>
  </div>
</template>

<script lang="ts">
import { Vue } from 'vue-class-component';

export default class Profile extends Vue {}
</script>

<style scoped lang="scss">
.profile {
  background: transparent linear-gradient(210deg, #3F68EA 0%, #252731 100%) 0% 0%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 60px 40px;

  img.profile-image {
    width: 250px;
    border-radius: 50%;
    padding: 20px;

    @include media($from: "lg") {
      width: 400px;
    }
  }

  .image-border {
    position: absolute;
    width: 290px;
    height: 290px;
    background-image: url("data:image/svg+xml,%3csvg width='100%25' height='100%25' xmlns='http://www.w3.org/2000/svg'%3e%3crect width='100%25' height='100%25' fill='none' rx='300' ry='300' stroke='%23FFFFFF' stroke-width='8' stroke-dasharray='100%2c 70%2c 20' stroke-dashoffset='0' stroke-linecap='butt'/%3e%3c/svg%3e");
    border-radius: 300px;

    @include media($from: "lg") {
      width: 445px;
      height: 445px;
    }
  }

  h1, h2, h3 {
    text-transform: uppercase;
  }

  h1 {
    margin-top: 80px;
  }

  .info {
    width: 100%;
    margin-top: 60px;
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 42px;
    font-weight: 900;

    @include media($from: "lg") {
      flex-direction: row;
      justify-content: space-evenly;
    }

    div {
      display: flex;
      align-items: center;
    }
  }

  h3 {
    font-size: 50px;
    font-weight: 900;
    margin-top: 60px;
    text-align: center;
  }

  p {
    font-size: 24px;
    font-weight: 600;
    text-align: center;
    margin: 35px 0;
  }
}
</style>
