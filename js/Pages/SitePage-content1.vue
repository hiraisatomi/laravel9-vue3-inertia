<script setup>
import { ref } from 'vue';
</script>

<template>
<div>
  <h2>SitePage-content1</h2>
  <p>samplesamplesamplesamplesamplesample
    <br>samplesamplesamplesamplesample
    samplesamplesamplesamplesample</p>
    <p>samplesamplesamplesamplesamplesample
    <br>samplesamplesamplesamplesample
    samplesamplesamplesamplesample</p>
    <p>samplesamplesamplesamplesamplesample
    <br>samplesamplesamplesamplesample
    samplesamplesamplesamplesample</p>
</div>
</template>

<style scoped>
div {
  width: 100%;
  word-wrap: break-word;
}

h2 {
  color: rgba(91, 139, 183, 0.7);
}

@media screen and (max-width: 795px) { /* sp用スタイル */
  p {
    font-size: 10px;
  }

}
</style>