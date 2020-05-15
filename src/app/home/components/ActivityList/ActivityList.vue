<template>
  <div>
    <li v-for="activity in activities" :key="activity.id">
      <div>
        <activity v-bind:activity="activity" />
      </div>
    </li>
  </div>
</template>
<script lang="ts">
// TODO: figureout the meta data
import axios from 'axios';
import Activity from '../Activity/Activity.vue';

export default {
  data() {
    return {
      activities: [],
    };
  },
  mounted() {
    console.log('this runs when the activity list is mounted');

    this.activities = require('./activity.json');
    console.log(this.activities);
  },
  components: {
    Activity,
  },
};
</script>
