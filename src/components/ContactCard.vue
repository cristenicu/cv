<template>
  <div class="contact-card">
    <i class="uil" :class="`uil-${icon}`"></i>
    <div class="contact-card__info">
      <label>{{ label }}</label>
      <slot />
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Options } from 'vue-class-component';

@Options({
  props: {
    icon: String,
    label: String,
  },
})
export default class ContactCard extends Vue {}
</script>

<style scoped lang="scss">
.contact-card {
  background-color: #1E1F27;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 15px;
  border-radius: 24px;
  margin-top: 20px;
  max-width: 100%;
  font-size: 24px;
  font-weight: 900;

  @include media($from: "lg") {
    padding: 30px;
    font-size: 30px;
  }

  i {
    &::before {
      background: linear-gradient(40deg, #4044E3, #3ED8FF);
      background-clip: text;
      -webkit-text-fill-color: transparent;
      -moz-text-fill-color: transparent;
    }

    background: linear-gradient(40deg, #22253B, #20323D);
    font-size: 24px;
    margin-right: 30px;
    border-radius: 50%;
    min-width: 50px;
    min-height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;

    @include media($from: "lg") {
      font-size: 34px;
      min-width: 70px;
      min-height: 70px;
    }
  }

  &__info {
    display: flex;
    flex-direction: column;

    label {
      color: #9D9DA3;
      font-size: 18px;
      font-weight: 600;
    }

    @include media($from: "lg") {
      font-size: 24px;
    }
  }
}
</style>
