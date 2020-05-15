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
    axios.get('https://lfg-stub.herokuapp.com/activity/1713/groups').then((response) => (this.activities = response));
    console.log(this.activities);
  },
  components: {
    Activity,
  },
};
</script>
