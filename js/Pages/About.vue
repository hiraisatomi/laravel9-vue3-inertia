<script setup>
import NavbarVue from './Navbar.vue';
import SitePageContent1Vue from './SitePage-content1.vue';
</script>

<template>
<div>
  <div><NavbarVue /></div>
  <div class="content">
    <h1>About</h1>
    <p>samplesamplesamplesamplesamplesample
      <br>samplesamplesamplesamplesample
      samplesamplesamplesamplesample</p>
      <p>samplesamplesamplesamplesamplesample
      <br>samplesamplesamplesamplesample
      samplesamplesamplesamplesample</p>
      <p>samplesamplesamplesamplesamplesample
      <br>samplesamplesamplesamplesample
      samplesamplesamplesamplesample
    </p>
    <SitePageContent1Vue />
    <div class="btn_area"><a class="btn" href="./">Topへ戻る</a></div>
    </div>
</div>
</template>

<style>
html, body {
  margin: 0;
}

div {
  text-align: center;
  word-wrap: break-word;
}

.content {
  padding: 100px 20px;
}

h1 {
  color: rgba(91, 139, 183);
}
.btn_area {
  margin: 30px auto;
}

.btn {
  padding: 10px;
  background-color: rgba(36, 139, 105, 0.6);
  border-radius: 6px;
  cursor: pointer;
  color: white;
  width: 100px;
  text-decoration: none;
}

@media screen and (max-width: 795px) { /* sp用スタイル */
  p {
    font-size: 10px;
  }

}
</style>