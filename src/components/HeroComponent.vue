<script>
export default {};
</script>
<template>
  <v-container class="hero-wrapper">
    <div class="hero-wrapper__text">
      Go wherever, <br />
      whenever
    </div>
    <div class="hero-wrapper__sub-text">
      Bolt is the all-in-one mobility app. Get picked up by a <br />
      top-rated driver in minutes and enjoy a comfortable ride <br />
      to wherever you’re going; or skip the traffic entirely on <br />
      one of our industry-leading scooters.
    </div>
    <div class="hero-wrraper__cta">
      <v-btn elevation="2" size="x-large" class="text-none" color="success" rounded="xl"
        >Get the app</v-btn
      >
    </div>
  </v-container>
</template>
<style lang="scss" scoped>
.hero-wrapper {
  color: #ffffff;
  padding: 0px 40px !important;

  &__text {
    font-size: 4rem;
    letter-spacing: -0.01em;
    // letter-spacing: 1px;
    line-height: 4.5rem;
    font-weight: 750;
    margin: 25px 0;
  }

  &__sub-text {
    margin: 40px 0;
    font-size: 1.25rem;
    line-height: 1.75rem;
  }
}
.v-btn__content {
  font-size: 1.3rem !important;
  font-weight: 600 !important;
}
</style>
