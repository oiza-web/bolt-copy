<script>
import DriverSection from './DriverSection.vue';
import courierImage from '../assets/images/feature-courier.webp';
import restaurantImage from '../assets/images/feature-restaurant-payment.webp';
import driverImage from '../assets/images/bolt-car-driver.jpg';
import fleetImage from '../assets/images/feature-tesla-fleet.webp';
export default {
    components: { DriverSection },
    data: () => ({
        tab: null,
        tabItems: [
            {
                content: {
                    title: 'Drive and earn money',
                    image: driverImage,
                    details: [
                        {
                            number: '1',
                            heading: 'Drive more, earn more',
                            description: 'Our 150+ million riders will send you plenty of ride requests. When demand is high, you can earn even more.'
                        },
                        {
                            number: '2',
                            heading: 'Set your schedule',
                            description: 'Drive for as long and as often as you like. Weekdays; weekends; evenings — fit driving around your lifestyle.'
                        },
                        {
                            number: '3',
                            heading: 'Get paid each week',
                            description: `You'll receive your earnings at the end of each week — no need to wait around for payday.`
                        }
                    ],
                    btnLabel: 'Learn more'
                }
            },
            {
                content: {
                    title: 'Make money delivering food',
                    image: courierImage,
                    details: [
                        {
                            number: '1',
                            heading: 'Earn extra income, fast',
                            description: `There's no subscription fee.You'll receive your earnings at the end of each week.`
                        },
                        {
                            number: '2',
                            heading: 'Make money whenever you like',
                            description: `You decide when and how often you deliver — weekdays, evenings, weekends, or just the occasional hour — it's up to you.`
                        },
                        {
                            number: '3',
                            heading: 'Deliver your way',
                            description: 'Bike, scooter or car — you choose how to make deliveries.'
                        }
                    ],
                    btnLabel: 'Learn more'
                }
            },
            {
                content: {
                    title: 'Increase your sales',
                    image: restaurantImage,
                    details: [
                        {
                            number: '1',
                            heading: 'Reach new customers',
                            description: 'Millions of our users are ordering food or goods from restaurants and stores just like yours.'
                        },
                        {
                            number: '2',
                            heading: 'Increase your earnings',
                            description: 'Our large network of users brings more customers and business to you.'
                        },
                        {
                            number: '3',
                            heading: 'Let us handle delivery',
                            description: `We'll take care of the logistics, while you focus on running your business.`
                        }
                    ],
                    btnLabel: 'Learn more'
                }
            },
            {
                content: {
                    title: 'Grow your transport business',
                    image: fleetImage,
                    details: [
                        {
                            number: '1',
                            heading: 'Boost your earnings',
                            description: 'Our large rider community means more orders per day and higher earnings.'
                        },
                        {
                            number: '2',
                            heading: 'Manage your assets',
                            description: 'Easily view your vehicles, drivers and their current status.'
                        },
                        {
                            number: '3',
                            heading: 'Keep track of performance',
                            description: `Get easy access to each driver's completed trips, invoices, and payout information.`
                        }
                    ],
                    btnLabel: 'Learn more'
                }
            }
        ]
    })
}
</script>
<template>
    <v-container class="earn-money-container">
        <div class="section__title">Earn money with Bolt</div>
        <div class="section__subtitle">
            <div class="section__switch-tabs">
                <div>
                    <v-tabs v-model="tab">
                        <v-tab value="driver" class="text-none mx-4" size="small" rounded="xl"
                            variant="outlined">Driver</v-tab>
                        <v-tab value="courier" class="text-none mx-4" size="small" rounded="xl"
                            variant="outlined">Courier</v-tab>
                        <v-tab value="restaurant" class="text-none mx-4" size="small" rounded="xl"
                            variant="outlined">Restaurant or
                            store owner</v-tab>
                        <v-tab value="fleet" class="text-none mx-4" size="small" rounded="xl" variant="outlined">Fleet
                            owner</v-tab>
                    </v-tabs>

                    <v-card-text>
                        <v-tabs-window v-model="tab">
                            <v-tabs-window-item value="driver">
                                <DriverSection :content="tabItems[0].content" />
                            </v-tabs-window-item>

                            <v-tabs-window-item value="courier">
                                <DriverSection :content="tabItems[1].content" />
                            </v-tabs-window-item>

                            <v-tabs-window-item value="restaurant">
                                <DriverSection :content="tabItems[2].content" />
                            </v-tabs-window-item>
                            <v-tabs-window-item value="fleet">
                                <DriverSection :content="tabItems[3].content" />
                            </v-tabs-window-item>
                        </v-tabs-window>
                    </v-card-text>
                </div>
            </div>
        </div>
    </v-container>
</template>
<style lang="scss">
.earn-money-container {
    padding: 0px 40px !important;
    margin-top: 180px;

    .section {
        &__title {
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 3rem;
            font-weight: 700;
            color: #2e313f;
            letter-spacing: 0.1px;
        }

        &__switch-tabs {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
        }
    }
}

.driver-wrapper {
    max-width: 1400px;
    min-width: 1200px;
    height: 690px;
    padding: 30px 20px;
}

.driver-bolt__picture {
    padding-right: 100px;
}

.driver-bolt__picture img {
    height: 450px;
    width: 560px;
    border-radius: 10px;
}

.driver-bolt__earn-money-details__number {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 20px;
    width: 20px;
    font-size: 12px;
    font-weight: 700;
    color: #ffffff;
    border-radius: 150px;
    text-align: center;
    background-color: #32BA78;

    p {
        color: #B2B5BA;
    }
}

.v-tab.v-tab.v-btn {
    height: 40px !important;
}

.v-slide-group__content {
    justify-content: center;
}

.v-tab--selected {}
</style>
