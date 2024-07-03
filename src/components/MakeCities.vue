<script>
import DriverSection from './DriverSection.vue';
import boltCities from '../assets/images/feature-cities-for-people.webp'
export default {
    components: { DriverSection },
    data: () => ({
        content: {
            title: 'Making cities for people, not cars',
            subtitle: 'By sharing our knowledge of the industry and real-time data we’re helping to improve our cities.',
            image: boltCities,
            details: [
                {
                    number: '1',
                    heading: 'Sharing best practices',
                    description: 'We’re able to provide insights that help local authorities make their cities more connected and liveable.'
                },
                {
                    number: '2',
                    heading: 'One app, many ways to move',
                    description: 'With multiple transport services inside a single app, getting around safely, in a more sustainable way, has never been easier.'
                },
                {
                    number: '3',
                    heading: 'Less is more',
                    description: `Shared transport can transform our cities by lowering emissions, reducing congestion, and the demand for parking spaces.`
                }
            ],
            btnLabel: 'Learn more'
        }
    }),
    setup(){
        return{}
    }
}
</script>
<template>
    <v-container>
        <DriverSection :content="content" :subtitle="true" :has-button="true" :has-left-image="false" />
    </v-container>
</template>



<style lang="scss" scoped></style>