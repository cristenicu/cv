<template>
  <div class="skill">
    <div class="title"><slot /></div>
    <div class="progress">
      <div class="progress-indicator" :style="`width: ${progress}%`"></div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    progress: String,
  },
})
export default class Skill extends Vue {}
</script>

<style scoped lang="scss">
.skill {
  .title {
    font-size: 50px;
    font-weight: 900;
    margin-top: 30px;
  }

  .progress {
    width: 100%;
    height: 18px;
    background-color: #13141A;
    border-radius: 30px;
    margin-top: 20px;

    &-indicator {
      height: 18px;
      border-radius: 30px;
      background: linear-gradient(90deg, #4040E3, #3EDAFF);
    }
  }
}
</style>
