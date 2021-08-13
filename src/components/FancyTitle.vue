<template>
  <h1 class="fancy-title" :class="{stylish: stylish}"><slot /></h1>
</template>

<script lang="ts">
import { Vue, Options } from 'vue-class-component';

@Options({
  props: {
    stylish: {
      type: Boolean,
      default: false,
    },
  },
})
export default class FancyTitle extends Vue {}
</script>

<style scoped lang="scss">
.fancy-title {
  margin-top: 45px;
  background: linear-gradient(260deg, #DEEDF0, #7986A3);
  background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  width: fit-content;

  &.stylish {
    background: linear-gradient(260deg, #FF8F65, #E440CB);
    background-clip: text;
  }
}

</style>
