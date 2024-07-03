<script setup>
import NavBar from "../components/NavBar.vue";
import HeroComponent from "../components/HeroComponent.vue";
import EarnMoney from "../components/EarnMoney.vue";
import MakeCities from "../components/MakeCities.vue";
import BoltBuilding from "../components/BoltBuilding.vue";
import DownloadApp from "../components/DownloadApp.vue";
</script>

<template>
  <main class="container">
    <NavBar />
    <HeroComponent />
    <EarnMoney />
    <MakeCities />
    <BoltBuilding />
    <DownloadApp />
  </main>
</template>

<style lang="scss">
.container {
  background-image: url("../assets/images/hero-img-3.jpg");
  height: 650px;
  background-repeat: no-repeat;
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
}
</style>
