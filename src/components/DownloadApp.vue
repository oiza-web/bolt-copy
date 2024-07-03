<script>
import { } from 'vue'

export default {
    data: () => ({
        tab: null,
    })
}
</script>

<template>
    <v-container>
        <div class="section__title text-center text-h3 font-weight-bold mb-6">Download our apps</div>
        <v-tabs v-model="tab">
            <v-tab value="Rides" class="text-none mx-4 text-subtitle-2" size="small" rounded="xl"
                variant="outlined">Driver</v-tab>
            <v-tab value="Delivery" class="text-none mx-4 text-subtitle-2" size="small" rounded="xl"
                variant="outlined">Courier</v-tab>
        </v-tabs>
        <div class="rounded-xl" style="background-color: #1d965c; height: 600px !important;">
            <div class="download-app__wrapper w-full d-flex justify-space-between align-center px-16">
                <div class="download-app__wrapper-text-section">
                    <div class="download-app__wrapper-text-section-title text-h3 font-weight-bold text-white">
                        Your favourite food, <br>delivered fast.
                    </div>
                    <div class="download-app__wrapper-text-section-subtitle text-h6 text-white my-6">
                        Available for iOS and Android devices.
                    </div>
                    <v-btn rounded class="text-none mt-6 text-black font-weight-bold" elevation="0">Get the app</v-btn>
                </div>
                <div class="download-app__wrapper-image-section">
                    <img class="mt-8" src="../assets/images/bolt-mobile-phone.webp" height="500" alt="" srcset="">
                </div>
            </div>
        </div>
    </v-container>
</template>
<style lang="scss" scoped></style>