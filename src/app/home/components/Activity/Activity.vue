<template>
  <div>
    <!-- TODO: make this look pretty -->
    <img :src="activity.image" />
    <div>Member Count: {{ activity.memberCount }}</div>
    <div>Slots available: {{ activity.slotsAvailable }}</div>
    <div>Description: {{ activity.description }}</div>
    <div>Total Members: {{ activity.totalMembers }}</div>

    Members:
    <li v-for="member in activity.members">Name: {{ member.alias }}</li>
    <br />

    Games:
    <li v-for="game in activity.activity">
      <span>
        Name: {{ game.name }}<br />
        Platform: {{ game.platform.name }}
      </span>
    </li>
  </div>
</template>
<script lang="ts">
export default {
  props: ['activity'],
};
</script>
