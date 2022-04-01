<template>
  <p>
    <strong> {{ time }} - {{ title }}</strong
    ><br />
    {{ text }} <br />
    <img
      v-if="imageSrc != null"
      :src="require(`../assets/${imageSrc}`)"
      style="width: 400px; height: 290px; margin-top: 0.5em"
    />
    <audio
      ref="audio"
      controls
      v-if="audioSrc !== null"
      :src="audioSrc"
      style="height: 1.5em; margin-top: 0.5em"
    >
      <source src="" type="audio/mpeg" />
      Your browser does not support the audio element.
    </audio>
    <iframe v-if="isVideo"
      width="560"
      height="315"
      src="https://www.youtube.com/embed/oh0JJcf4z6A"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
  </p>
</template>

<script>
export default {
  name: "Entry",
  props: {
    title: String,
    text: String,
    time: String,
    imageSrc: String,
    audioSrc: String,
    isVideo: Boolean,
  },
};
</script>
