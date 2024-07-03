<script>
import DriverSection from './DriverSection.vue';
import boltBuildings from '../assets/images/feature-bolt-building.webp'
export default {
    components: { DriverSection },
    data: () => ({
        content: {
            title: 'À Propos',
            subtitle: 'Bolt is the first European mobility super-app. We’re making cities for people, offering better alternatives for every purpose a private car serves — including ride-hailing, shared cars, scooters, and food and grocery delivery.',
            image: boltBuildings,
            details: [
                {
                    number: '1',
                    heading: '150+ million',
                    description: 'customers around the world.'
                },
                {
                    number: '2',
                    heading: '5 continents',
                    description: '45+ countries'
                },
                {
                    number: '3',
                    heading: '3.1+ million',
                    description: `drivers and couriers.`
                }
            ],
        }
    })
}
</script>
<template>
    <v-container>
        <DriverSection :content="content" :subtitle="true" :has-button="false" :has-left-image="true"/>
    </v-container>
</template>



<style lang="scss" scoped></style>