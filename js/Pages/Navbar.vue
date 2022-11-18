<script setup>
import { ref } from 'vue';
</script>

<template>
<div>
  <div class="header_content">
    <div class="hamburger-menu">
      <input type="checkbox" id="menu-btn-check" class="checkbox_hidden">
      <label for="menu-btn-check" class="menu-btn"><span></span></label>
          <!-- ここからヘッダーメニュー -->
        <div class="menu-content">
          <ul class="menu-content_box">
            <li class="menu-content_text"><a class="menubtn" href="/">Home</a></li>
            <li class="menu-content_text"><a class="menubtn" href="/about">about</a></li>
            <li class="menu-content_text"><a class="menubtn" href="/sitepage">sitepage</a></li>
            <li class="menu-content_text"><a class="menubtn salonreserve" href="#" target="_blank" rel="noopener">外部リンク</a></li>
            <!-- <li class="menu-content_text"><a class="menubtn" href="外部リンク" target="_blank" rel="noopener"><img class="sns_icon" src="./assets/images/facebook.png"></a></li> -->
          </ul>
        </div>
    </div>
  </div>
</div>
</template>

<style>
/* header */
.checkbox_hidden {
  display: none;
}

.header_content {
  display: flex;
  position: fixed;
  z-index: 2;
  align-items: center;
  text-decoration: none;
  justify-content: space-between;
  width: 100%;
  background-color: rgba(91, 139, 183, 0.7);
  box-sizing: border-box;
}

@media screen and (min-width: 796px) { /* pc用スタイル */
  /* headerエリア */
  .header_content {
    justify-content: center;
  }

  .menu-content_box {
    padding: 0;
    display: flex;
    align-items: center;
  }

  .menu-content_text {
    list-style: none;
  }

  .menubtn {
    margin: 10px 20px;
    color: rgba(75, 74, 95, 0.9);
    text-decoration: none;
    font-size: 13px;
  }

  .menubtn:hover {
    border-bottom: 1px solid rgba(75, 74, 95, 0.9);
    opacity: 0.6;
  }
}

@media screen and (max-width: 795px) { /* sp用スタイル */
  .menu-btn {
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    top: 14px;
    right: 10%;
    height: 30px;
    width: 30px;
    z-index: 90;
  }

  .menu-btn span {
    content: "";
    display: block;
    height: 1px;
    width: 20px;
    right: 20%;
    border-radius: 2px;
    background-color: rgba(75, 74, 95, 0.9);
    position: absolute;
  }

  .menu-btn span:before {
    content: "";
    display: block;
    height: 1px;
    width: 20px;
    right: 0;
    border-radius: 2px;
    background-color: rgba(75, 74, 95, 0.9);
    position: absolute;
  }

  .menu-btn span:after {
    content: "";
    display: block;
    height: 1px;
    width: 20px;
    right: 0;
    border-radius: 2px;
    background-color: rgba(75, 74, 95, 0.9);
    position: absolute;
  }

  .menu-btn span:before {
    bottom: 7px;
  }

  .menu-btn span:after {
    top: 7px;
  }

  /* 3本線をクリック後バッテンに */
  #menu-btn-check:checked ~ .menu-btn span {
    background-color: rgba(255, 255, 255, 0);
  }

  #menu-btn-check:checked ~ .menu-btn span:before {
    bottom: 0;
    width: 20px;
    transform: rotate(45deg);
    background-color: rgba(75, 74, 95, 0.9);
  }

  #menu-btn-check:checked ~ .menu-btn span:after {
    top: 0;
    width: 20px;
    transform: rotate(-45deg);
    background-color: rgba(75, 74, 95, 0.9);
  }

  /* メニューが閉じている時は表示枠外に隠す */
  .menu-content {
    width: 100%;
    height: 1000px;
    position: fixed;
    top: 0;
    left: 100%;
    z-index: 80;
    padding-top: 100px;
    background-color: white;
    /* background-image: url(../../../images/background-water.png); */
    transition: all 0.7s;
  }

  .menu-content_box,.menu-content_text {
    border-bottom: none;
    text-align: center;
    list-style: none;
    padding: 0;
  }

  .menu-btn {
    display: block;
    padding: 10px;
    position: relative;
  }

  .menu-content_text,.menubtn {
    display: block;
    font-size: 16px;
    box-sizing: border-box;
    color: rgba(75, 74, 95, 0.9);
    text-decoration: none;
    padding: 5px 10px;
    position: relative;
  }

  .menubtn.salonreserve {
    width: 150px;
    margin: 0 auto;
  }

  #menu-btn-check:checked ~ .menu-content {
    left: 0;
    width: 100%;
    height: 1000px;
  }
}
</style>