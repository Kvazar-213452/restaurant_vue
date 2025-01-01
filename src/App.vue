<template>
  <MenuComponent :msg="unixw"/>
  <MainComponent/>
  <FouterComponent/>
</template>

<script>
import MenuComponent from "./components/MenuComponent.vue"
import MainComponent from "./components/MainComponent.vue"
import FouterComponent from "./components/FouterComponent.vue"

export default {
  data() {
    return {
      unixw: "ddqws",
    };
  },
  components: {
    MenuComponent,
    MainComponent,
    FouterComponent
  }
}
</script>

<style>

</style>
