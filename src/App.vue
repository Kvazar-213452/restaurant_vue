<!--  ⣾⡇⣿⣿⡇⣾⣿⣿⣿⣿⣿⣿⣿⣿⣄⢻⣦⡀⠁⢸⡌⠻⣿⣿⣿⡽⣿⣿
      ⡇⣿⠹⣿⡇⡟⠛⣉⠁⠉⠉⠻⡿⣿⣿⣿⣿⣿⣦⣄⡉⠂⠈⠙⢿⣿⣝⣿
      ⠤⢿⡄⠹⣧⣷⣸⡇⠄⠄⠲⢰⣌⣾⣿⣿⣿⣿⣿⣿⣶⣤⣤⡀⠄⠈⠻⢮
      ⠄⢸⣧⠄⢘⢻⣿⡇⢀⣀⠄⣸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣧⡀⠄⢀
      ⠄⠈⣿⡆⢸⣿⣿⣿⣬⣭⣴⣿⣿⣿⣿⣿⣿⣿⣯⠝⠛⠛⠙⢿⡿⠃⠄⢸
      ⠄⠄⢿⣿⡀⣿⣿⣿⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⣿⣿⣿⣿⡾⠁⢠⡇⢀
      ⠄⠄⢸⣿⡇⠻⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣏⣫⣻⡟⢀⠄⣿⣷⣾
      ⠄⠄⢸⣿⡇⠄⠈⠙⠿⣿⣿⣿⣮⣿⣿⣿⣿⣿⣿⣿⣿⡿⢠⠊⢀⡇⣿⣿
      ⠒⠤⠄⣿⡇⢀⡲⠄⠄⠈⠙⠻⢿⣿⣿⠿⠿⠟⠛⠋⠁⣰⠇⠄⢸⣿⣿⣿ -->

<template>
  <div class="main">
    <MenuComponent />
    <div class="main_sect" style="background-image: url(/images/cover.png)">
      <br><br><br><br><br><br><br><br><br>
      <div class="dest_main_div">
        <p class="dest_main">Free delivery of pizza and sushi in New York</p>
        <br><br><br>
        <p class="desc_unix">We work from 10:00 to 22:00</p>
        <br>
        <p class="desc_unix">+1 123 456 7890</p>
      </div>
    </div>
    <br>
    <div class="content">
      <div :id="key" v-for="(group, key) in goods" :key="key">
        <p class="name_key">{{ key }}</p>
        <div class="unix"><GoodsComponent v-for="(el, idx) in group" :key="idx" :goods="el" /></div>
      </div>
    </div>
    <br><br>
    <FouterComponent />
  </div>
</template>

<script>
import MenuComponent from "./components/MenuComponent.vue";
import GoodsComponent from "./components/GoodsComponent.vue";
import FouterComponent from "./components/FouterComponent.vue";
import goodsData from "./assets/goods.json";

export default {
  data() {
    return {
      goods: goodsData
    };
  },
  components: {
    MenuComponent,
    GoodsComponent,
    FouterComponent
  }
};
</script>
