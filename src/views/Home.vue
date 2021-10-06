<template>
  <div class="cv">
    <profile class="cv__profile" />

    <contact class="cv__contact" />

    <div class="cv__main">
      <fancy-title>Experience</fancy-title>
      <section v-for="job in jobs" :key="job.start" class="cv__item">
        <div class="cv__item-header">
          <h4>{{ job.title }} @ {{ job.company }}</h4>
          <span>
            <i class="uil uil-calendar-alt" />
            {{ job.start }} - {{ job.end }}
          </span>
        </div>
        <p class="cv__item-content">{{ job.description }}</p>
      </section>

      <fancy-title>Education</fancy-title>
      <section v-for="ed in education" :key="ed.start" class="cv__item">
        <div class="cv__item-header">
          <h4>{{ ed.school }}</h4>
          <span>
            <i class="uil uil-calendar-alt" />
            {{ ed.start }} - {{ ed.end }}
          </span>
        </div>
        <p class="cv__item-content">{{ ed.description }}</p>
      </section>

      <fancy-title>Skills</fancy-title>
      <section class="skills">
        <skill progress="80">PHP</skill>
        <skill progress="70">Laravel</skill>
        <skill progress="90">VueJS</skill>
        <skill progress="50">Websockets</skill>
      </section>

      <fancy-title stylish>Portfolio</fancy-title>
      <p>I don't really have a portfolio but I have a github account with some repos :D</p>
      <super-link url="https://github.com/cristenicu?tab=repositories">https://github.com/cristenicu</super-link>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Profile from '@/components/Profile.vue';
import Contact from '@/components/Contact.vue';
import Skill from '@/components/Skill.vue';
import FancyTitle from '@/components/FancyTitle.vue';
import SuperLink from '@/components/SuperLink.vue';

@Options({
  components: {
    Profile,
    Contact,
    Skill,
    FancyTitle,
    SuperLink,
  },
})
export default class Home extends Vue {
jobs = [
  {
    title: 'Full Stack Developer',
    company: 'Globant',
    start: '2020',
    end: 'present',
    description: 'ReactJS, NodeJS, MySql, Android, Flutter (just a little bit), Docker/Kubernetes, Google Assistant, Firebase',
  },
  {
    title: 'Web Developer',
    company: 'CodeValley Software [Startup]',
    start: '2018',
    end: '2020',
    description: 'VueJS',
  },
  {
    title: 'Web Developer',
    company: 'Yonder',
    start: '2018',
    end: '2020',
    description: 'PHP (Laravel), Android, Typescript (ReactJS)',
  },
  {
    title: 'Full Stack Developer',
    company: 'Array51',
    start: '2017',
    end: '2018',
    description: 'PHP (Laravel), Javascript (ReactJS)',
  },
  {
    title: 'Full Stack Developer',
    company: 'Wolfpack Digital',
    start: '2016',
    end: '2017',
    description: 'AWS, PHP (Laravel), MySql, VueJS, Firebase, Android',
  },
  {
    title: 'Full Stack Developer',
    company: 'E&M',
    start: '2015',
    end: '2016',
    description: 'PHP (Laravel), HTML, CSS, JQuery, VueJS, Websockets, MySQL, Java (JSF + Primefaces), Android, Linux Server',
  },
  {
    title: 'Full Stack Developer',
    company: 'Projects  Abroad',
    start: '2013',
    end: '2015',
    description: 'PHP (Zend, Symfony), HTML, CSS, Javascript, MySql',
  },
  {
    title: 'Full Stack Developer',
    company: 'DM Elektron',
    start: '2012',
    end: '2013',
    description: 'PHP, HTML, CSS, Javascript, MySql',
  },
  {
    title: 'Programmer',
    company: 'Ipsos Interactive Services',
    start: '2010',
    end: '2012',
    description: '',
  },
]

education = [
  {
    school: 'Bachelor of Engineering (B.E.)',
    start: '2006',
    end: '2010',
    description: 'Electrical, Electronics and Communications Engineering',
  },
]
}
</script>

<style lang="scss" scoped>
.cv {
  color: white;
  display: grid;
  grid-template-rows: auto;
  grid-template-columns: 1fr;
  grid-template-areas:
    "profile"
    "contact"
    "main";

  @include media($from: "md") {
    grid-template-columns: 1fr 1fr;
    grid-template-areas:
      "profile contact"
      "main main";
  }

  @include media($from: "lg") {
    grid-template-columns: 1fr 2fr;
    grid-template-areas:
      "profile main"
      "contact main";
  }

  &__profile {
    grid-area: profile;
  }

  &__contact {
    grid-area: contact;
  }

  &__main {
    grid-area: main;
    background-color: #1E1F27;
    display: flex;
    flex-direction: column;
    padding: 20px;

    @include media($from: "md") {
      padding: 50px;
    }
  }

  .cv__item {
    display: flex;
    flex-direction: column;
      margin: 25px 0;

    &-header {
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      @include media($from: "lg") {
        flex-direction: row;
      }

      span {
        font-size: 24px;
      }

      i {
        background: #35363D;
        border-radius: 50%;
        width: fit-content;
        min-width: 40px;
        min-height: 40px;
        display: inline-flex;
        align-items: center;
        justify-content: center;
      }
    }

    &-content {
      margin-top: 14px;
    }
  }

  .skills {
    display: grid;
    grid-template-columns: 1fr;

    @include media($from: 'md') {
      grid-template-columns: 1fr 1fr;
      gap: 40px;
    }
  }
}
</style>
