<template>
  <li class="timeline-event">
    <label class="timeline-event-icon"></label>
    <div class="timeline-event-copy">
      <p class="timeline-event-thumbnail">{{ title }}</p>
      <!-- eslint-disable-next-line vue/valid-v-for -->
      <Entry v-for="entry in entries" :key="entry.time" :time="entry.time" :title="entry.title" :text="entry.text" :imageSrc="entry.imageSrc" :audioSrc="entry.audioSrc" :isVideo="entry.isVideo || false"/>
    </div>
  </li>
</template>

<script>
import Entry from './Entry.vue';
export default {
  components: { Entry },
  name: "Day",
  props: {
    title: String,
    entries: Array,
  },
};
</script>

<style scoped>
</style>
