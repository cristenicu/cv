<template>
  <a :href="url" class="super-link">
    <i class="uil uil-link" />
    <label><slot /></label>
  </a>
</template>

<script lang="ts">
import { Vue, Options } from 'vue-class-component';

@Options({
  props: {
    url: String,
  },
})
export default class SuperLink extends Vue {}
</script>

<style scoped lang="scss">
.super-link {
  background-color: #000;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 15px;
  border-radius: 62px;
  margin-top: 20px;
  font-size: 18px;
  font-weight: 900;
  text-decoration: none;
  width: fit-content;

  @include media($from: "lg") {
    padding: 25px;
    font-size: 50px;
  }

  i {
    &::before{
      background: linear-gradient(40deg, #FD8A6B, #FD8A6B);
      background-clip: text;
      -webkit-text-fill-color: transparent;
      -moz-text-fill-color: transparent;
    }

    background: linear-gradient(40deg, #261825, #281E1E);
    font-size: 24px;
    border-radius: 50%;
    min-width: 50px;
    min-height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;

    @include media($from: "md") {
      font-size: 34px;
      min-width: 70px;
      min-height: 70px;
    }
  }

  label {
    margin: 0 15px;
    cursor: pointer;

    @include media($from: "lg") {
      margin: 0 45px;
    }
  }
}
</style>
