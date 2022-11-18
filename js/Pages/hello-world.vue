<script setup>
// export default {
//     data() {
//         return {
//             greeting: "Hello World!",
//         };
//     },
// };
import CounterVue from './Counter.vue';
import Content1Vue from './Content1.vue';
import NavbarVue from './Navbar.vue';

const message = "よく使う単語や繰り返しのタイトルは変数を指定しよう";
</script>

<template>
    <div>
      <div class="navbar"><NavbarVue /></div>
      <div class="content">
        <p>{{ message }}</p>
        <h1>Hello world</h1>
        <p class="text">testtesttesttesttesttesttesttest</p>
        <CounterVue />
        <Content1Vue />
        <div class="btn_area"><a class="btn" href="/sitepage">sitepageへ</a></div>
        <div class="btn_area"><a class="btn" href="https://www.instagram.com/monami283103/?r=nametag" target="_blank" rel="noopener">snsリンクへ</a></div>
      </div>
    </div>
</template>

<style>
#app {
  text-align: center;
}

body {
  margin: 0;
}

div {
  word-wrap: break-word;
}



.content {
  padding: 100px 20px;
}

h1 {
  color: rgba(91, 139, 183);
}

.text {
  color: rgb(49, 55, 54);
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