<template>
<div class="container">
  <!-- 左側side bar -->
  <div class="side">
    <div class="name">CAT</div>
    <div class="social_link">
      <a href="https://www.tumblr.com/">
        <div class="icon_tumblr"></div>
      </a>
      <a href="https://tw.linkedin.com/">
        <div class="icon_linkedin"></div>
      </a>
      <a href="https://www.facebook.com/">
        <div class="icon_facebook"></div>
      </a>
  </div>
  </div>
  <!-- 右側 main section-->
  <div class="main">
    <div class="header">
      <ul>
        <li><a href="Home">Home</a></li>
        <li><a href="Home2">Home2</a></li>
        <li><a href="Article">Article</a></li>
        <li><a href="About">About</a></li>
        <li><a href="Location">Location</a></li>
        <li><a href="News">News</a></li>
        <li><a href="#"><img class="icon_search" src="src/assets/search_rounded.svg" alt="search_rounded"></a></li>
      </ul>
    </div>
    <!-- 手機版Header -->
    <div class="mobile_header">
      <div class="mobile_header_container">
        <div class="name">CAT</div>
        <div @click="menuOpen()">
          <img src="src/assets/toggle.png" alt="toggle">
        </div>
      </div>
      <div class="mobile_menu"
        v-if="viewStatus">
        <ul>
          <li><a href="Home">Home</a></li>
          <li><a href="Home2">Home2</a></li>
          <li><a href="Article">Article</a></li>
          <li><a href="About">About</a></li>
          <li><a href="Location">Location</a></li>
          <li><a href="News">News</a></li>
        </ul>
      </div>
    </div>   
    <!-- 手機版Header -->
    <div class="article">
      <div class="article_title">
        <div class="title_container">
          <div class="title_number">/ 01</div>
        </div>
        <div class="title_info_container">
          <div class="title_info active">About Cat</div>
          <div class="title_info">Senses</div>
          <div class="title_info">Behavior</div>
        </div>
      </div>
      <div class="article_detail">
        <div>EAT<br>EVERYDAY</div>
        <p>
          The cat is a domestic species of small carnivorous mammal.
          It is the only domesticated species in the family Felidae and is often referred to as the domestic cat to distinguish it from the wild members of the family.
        </p>
      </div>
    </div>
    <div class="footer">
      <div class="event col">
        <div class="col_title">EVENT</div>
        <div class="event_info">
          <div class="event_location">Cat’s Foods @Anythings About Cat Club</div>
          <div class="event_date">SF - Sat,July 14 / 15-17PM</div>
          <ul class="divide">
            <li><img src="src/assets/ellipse_active.png" alt="ellipse_active"></li>
            <li><img src="src/assets/ellipse_normal.png" alt="ellipse_normal"></li>
            <li><img src="src/assets/ellipse_normal.png" alt="ellipse_normal"></li>
          </ul>
        </div>
      </div>
      <div class="news">
        <div class="news_pic"><img src="src/assets/news_pic.png" alt="news_picture"></div>
        <div class="news_container">
          <div class="col_title">NEWS</div>
          <div class="news_info">
            The average lifespan of pet cats has risen in recent decades.
          </div>
          <div class="read_more">Read more</div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script setup>
  import {ref} from "@vue/reactivity"

  const viewStatus =ref(false) //手機版menu預設關閉
  
  //開啟menu
  const menuOpen = () => {
    viewStatus.value = !viewStatus.value
  }
</script>

<style scoped>
</style>