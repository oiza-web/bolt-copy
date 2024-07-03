<script setup>
import MoreOptions from "../components/MoreOptions.vue";
</script>
<template>
  <v-container class="main-container">
    <nav class="navigation">
      <div class="navigation__one">
        <div class="navigation__logo">
          <img src="../assets/images/bolt-logo-white.png" alt="" srcset="" />
        </div>
      </div>
      <div class="navigation__two">
        <div class="navigation__item">
          <div class="navigation__item-flag-icon">flag</div>
          <div class="navigation__item-flag-item">EN</div>
        </div>
        <div class="navigation__item">
          <v-btn rounded="xl" class="text-none" variant="text">Support</v-btn>
        </div>
        <div class="navigation__item-cta">
          <v-btn elevation="2" class="text-none" color="white" rounded="xl">Sign up</v-btn>
        </div>
        <div>
          <MoreOptions />
        </div>
      </div>
    </nav>
  </v-container>
</template>

<style lang="scss" scoped>
main-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: white;
}

.navigation {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 2400px;
  padding: 1rem;

  &__one {
    align-items: center;
    width: 100px;
  }

  &__two {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 480px;
  }

  &__logo {
    img {
      height: 40px;
    }

    cursor: pointer;
  }

  &__item {
    display: flex;
    align-items: center;
    font-size: 0.875rem !important;
    line-height: 1.25rem !important;
    font-weight: 600;
    color: #ffffff;
    cursor: pointer;

    &-flag-icon {
      margin-right: 0.5rem;
    }

    &-flag-item {
      margin-right: 1rem;
      font-size: 0.875rem !important;
      line-height: 1.25rem !important;
      font-weight: 600;
    }

    &-cta {
      font-weight: 700 !important;
    }
  }
}
</style>
