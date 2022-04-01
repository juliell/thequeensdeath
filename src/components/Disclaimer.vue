<template>
  <div @mouseover="showText = true" @mouseleave="showText = false">
    <img id="info-icon" alt="info Icon" src="../assets/info-blue.png" />
    <div id="disclaimer-text" v-show="showText" name="disclaimer">
      Die Ereignisse basieren auf dem Artikel <em>'London Bridge is down': the secret
      plan for the days after the Queen’s death</em> von Sam Knight, der 2017 im
      Guardian erschien. Im Rahmen des Storytelling-Projekts wurden die meisten Zeitstempel als auch einige
      erzählerischen Details hinzugefügt.
    </div>
  </div>
</template>


<script>
// import VModal from 'vue-js-modal';

export default {
  name: "Disclaimer",
  data: function () {
    return {
      showText: false,
    };
  },
};
</script>

<style scoped>
#info-icon {
  height: 2.5em;
  width: 2.5em;
  float: right;
  margin: 1.5em;
}

#disclaimer-text {
  z-index: 2;
  margin-right: 1em;
  position: absolute;
  right: 3em;
  top: 21em;
  width: 30em;
  text-align: left;
  border: 0.2em solid;
  padding: 0.25em;
  background-color: #25377c;
  color: white;
  font-family: "Perpetua", "Optima", "Garamond", "Times New Roman", Times, serif;
  font-size: 1.5em;
}
</style>