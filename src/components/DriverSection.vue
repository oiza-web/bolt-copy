<template>
    <div class="driver-wrapper d-flex justify-content-between">
        <div class="driver-bolt__picture" v-if="hasLeftImage">
            <img :src="content.image" alt="" srcset="" />
        </div>
        <div class="driver-bolt__earn-money" style="margin-right: 60px ;">
            <div class="driver-bolt__earn-money-title text-h4 font-weight-bold mb-4">
                {{ content.title }}
            </div>
            <div class="driver-bolt__earn-money-subtitle text-body-1 font-weight-bold mb-4" v-if="subtitle">
                {{ content.subtitle }}
            </div>
            <div class="driver-bolt__earn-money-details my-6" v-for="detail in content.details" :key="detail.number">
                <div class="driver-bolt__earn-money-details__one d-flex ">
                    <div class="driver-bolt__earn-money-details__number mt-1">
                        {{ detail.number }}
                    </div>
                    <div class="driver-bolt__earn-money-details__heading text-subtitle-1 font-weight-bold mx-4">
                        {{ detail.heading }}
                    </div>
                </div>
                <p class="ml-9 text-body-1">
                    {{ detail.description }}
                </p>
            </div>

            <v-btn v-if="hasButton" elevation="0" class="text-none font-weight-bold mt-6" size="large"
                color="grey-lighten-2" rounded="xl">
                {{ content.btnLabel }}
            </v-btn>
        </div>
        <div class="driver-bolt__picture" v-if="!hasLeftImage">
            <img :src="content.image" alt="" srcset="" />
        </div>
    </div>
</template>

<script>
export default {
    props: {
        content: {
            type: Object,
            required: true,
        },
        subtitle: {
            type: Boolean,
            required: false,
            default: false,
        },
        hasButton: {
            type: Boolean,
            required: false,
            default: true
        },
        hasLeftImage: {
            type: Boolean,
            default: true
        }
    },
    setup() {


        return {}
    }
}
</script>

<style lang="scss" scoped></style>