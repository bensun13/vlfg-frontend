<template>
  <div>
    <!-- TODO: figure out why the top level nav is on a different layer and how to make the viewport for the content-->
    <vue-headline style="padding-top:100px" level="2">LFG LIST SHOULD GO HERE</vue-headline>
    <activity-list />
  </div>
</template>

<script lang="ts">
import { mapState } from 'vuex';
import { IState } from '@/app/state';
import VueHeadline from '@components/VueHeadline/VueHeadline.vue';
import ActivityList from '../components/ActivityList/ActivityList.vue';

// TODO: figureout the meta data
export default {
  metaInfo: {
    title: 'vuesion - flexible, scalable, opinionated, fast',
    meta: [
      {
        name: 'description',
        content: 'LFG ',
      },
      {
        name: 'robots',
        content: 'INDEX,FOLLOW',
      },
      {
        name: 'keywords',
        content: 'valorant, lfg',
      },
      { name: 'og:site_name', content: 'LFG Valorant' },
      { name: 'og:type', content: 'website' },
      { name: 'og:locale', content: 'en' },
      { name: 'og:image:url', content: 'https://vuesion.herokuapp.com/logo.png' },
    ],
  },
  components: {
    VueHeadline,
    ActivityList,
  },
  computed: {
    ...mapState({}),
  },
};
</script>
