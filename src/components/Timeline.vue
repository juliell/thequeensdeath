<template>
  <ul class="timeline">
      <!-- eslint-disable-next-line vue/valid-v-for -->
      <Day v-for="day in days" :key="day.title" :title="day.title" :entries="day.entries" />
  </ul>
</template>

<script>
import Day from "./Day.vue";
import jsonData from "../data/data.json";

export default {
  components: { Day },
  name: "Timeline",
  data: function () {
    return { 
      days: []
    };
  },
  created() {
    this.days = jsonData.days;
  },
};
</script>


<style>
/* Fonts */
@import url(https://fonts.googleapis.com/css?family=Open+Sans:300,700);
body {
  font-size: 1em;
  font-weight: 300;
  line-height: 1.5;
  letter-spacing: 0.05em;
  box-sizing: border-box;
  background-color: #ececec;
}

/* Styling */
.timeline {
  margin: 4em auto;
  position: relative;
  max-width: 80em;
  list-style-type: none;
}
.timeline::before {
  background-color: #25377c;
  content: "";
  margin-left: -1px;
  position: absolute;
  top: 0;
  left: 2em;
  width: 2px;
  height: 100%;
}

.timeline-event {
  position: relative;
}

.timeline-event-copy {
  font-family: "Courier New", Courier, monospace;
  font-size: 1.2em;
  padding: 1.7em 1em 1em 0em;
  position: relative;
  top: -1.875em;
  left: 4em;
  width: 80%;
  text-align: left;
}

.timeline-event-copy > h3 {
  font-size: 1.75rem;
}

.timeline-event-copy > h4 {
  font-size: 1.2em;
  margin-bottom: 1.2em;
}

.timeline-event-copy > strong {
  font-weight: 700;
}

.timeline-event-copy > p {
  padding-bottom: 1.2em;
}

.timeline-event-copy > p.timeline-event-thumbnail {
  padding-bottom: 4px;
}

.timeline-event-icon {
  background-color: #25377c;
  outline: 12px solid white;
  display: block;
  margin: 0.5em 0.5em 0.5em -0.5em;
  position: absolute;
  top: 0;
  left: -0.5em;
  width: 1.2em;
  height: 1.2em;
  transition: 0.2s ease-in;
  transform: rotate(45deg);
}

.timeline-event-icon:hover {
  transform: rotate(-45deg);
  background-color: white;
  color: #25377c;
  outline: 10px solid #25377c;
}

.timeline-event-icon:hover > .timeline-event-thumbnail {
  transition: 0.5s ease-in 0.1s;
  box-shadow: inset 0 0 0 0em #25377c;
}

.timeline-event-thumbnail {
  color: white;
  font-family: "Perpetua", "Optima", "Garamond", "Times New Roman", Times, serif;
  font-size: 1.5em;
  font-weight: bold;
  display: inline-block;
  margin-bottom: 1.2em;
  margin-top: 0em;
  padding: 0.2em 1em 0.2em 1em;
  background-color: #25377c;
  transition: 0.5s ease-in 0.1s;
  box-shadow: inset 0 0 0 0em #25377c;
  width: 4em;
}

.timeline-event-thumbnail:hover {
  box-shadow: inset 40em 0 0 0 white;
  color: #25377c;
  outline: 8px solid #25377c;
}
</style>