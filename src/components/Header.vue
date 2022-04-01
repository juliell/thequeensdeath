<template>
  <div id="header">
    <img id="crest" src="../assets/crest-big-white.png" alt="Windsor Wappen" />
    <img id="coin" src="../assets/coin_trans_white.png" alt="5 pounds coin from 2020" />
    <p id="title">
      <strong>Die Königin ist tot. Lange lebe der König!</strong>
    </p>
    <div id="sec-title">Was passiert in den Tagen nach dem Tod <br> von Königin Elisabeth II.?</div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
#header {
  position: relative;
  top: 0;
  left: 0;
  height: 400px;
  background-color: #25377c;
}

#crest {
  float: left;
  color: white;
  width: 350px;
  padding-top: 2em;
  padding-left: 2em;
}

#coin{
  float: right;
   width: 330px;
  padding-top: 2em;
  padding-right: 2em;
}

#title {
  color: white;
  font-size: 3.75em;
  font-family: "Perpetua", "Optima", "Garamond", "Times New Roman", Times, serif;
  line-break: auto;
  text-align: center;
  padding-top: 100px;
  margin-bottom: 0.5em;
}

#sec-title {
  color: white;
  font-size: 2.75em;
  font-family: "Perpetua", "Optima", "Garamond", "Times New Roman", Times, serif;
  line-break: auto;
  text-align: center;
  margin-top: 0;
}
</style>