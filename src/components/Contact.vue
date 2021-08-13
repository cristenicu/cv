<template>
  <div class="contact">
    <h3>Contact</h3>

    <contact-card icon="phone" label="Phone number">
      +40743348757
    </contact-card>

    <contact-card icon="envelope" label="Email">
      criste_nicu@yahoo.com
    </contact-card>

    <contact-card icon="linkedin-alt" label="LinkedIn profile">
      <a href="https://www.linkedin.com/in/nicu-criste">linkedin.com/in/nicu-criste</a>
    </contact-card>

    <contact-card icon="apple">
      Mac
    </contact-card>
  </div>
</template>

<script lang="ts">
import { Vue, Options } from 'vue-class-component';
import ContactCard from '@/components/ContactCard.vue';

@Options({
  components: {
    ContactCard,
  },
})
export default class Contact extends Vue {}
</script>

<style scoped lang="scss">
.contact {
  background-color: #252731;
  display: flex;
  flex-direction: column;
  padding: 100px 20px;

  h3 {
    text-transform: uppercase;
  }
}
</style>
