<template>
  <v-container>
    <v-menu transition="slide-y-transition">
      <template v-slot:activator="{ props }">
        <v-btn variant="text" v-bind="props"> <img src="../assets/icons/menu.svg" alt="" srcset=""> </v-btn>
      </template>
      <v-list class="wrapper">
        <v-list-item v-for="(item, i) in items" :key="i">
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-container>
</template>
<script>

export default {
    data: () => ({
      items: [
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me 2' },
      ],
    }),
  }
</script>
<style lang="scss">
.v-menu > .v-overlay__content > .v-card, .v-menu > .v-overlay__content > .v-sheet, .v-menu > .v-overlay__content > .v-list{
    box-shadow: none !important;
    width: 1136px;
}
</style>
