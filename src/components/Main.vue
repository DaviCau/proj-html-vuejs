<template>
    <main>
        <section>
            <TransportSection :vehicles="vehicleTypes" />
        </section>
        <section class="dark_back">
            <Services :services="services" />
        </section>
        <!-- <section>

        </section> -->
        <section class="img_back">
            <Stats :stats="stats" />
        </section>
        <section class="dark_back">
            <Feedbacks :feedbacks="feedbacks" />
        </section>
        <!-- <section>

        </section> -->
    </main>
</template>

<script>
import TransportSection from './TransportSection.vue'
import Services from './Services.vue'
import Stats from './Stats.vue'
import Feedbacks from './Feedbacks.vue'

export default {
    name: "Main",
    data() {
        return {
            vehicleTypes: [
                {
                    imgUrl: "truck-1",
                    type: "Light",
                    maxWeight: "1200"
                },
                {
                    imgUrl: "truck-1",
                    type: "Medium",
                    maxWeight: "6000"
                },
                {
                    imgUrl: "truck-1",
                    type: "Heavy",
                    maxWeight: "24000"
                }
            ],
            services: [
                {
                    icon: "fas fa-truck-loading",
                    title: "Techology",
                    text: "We are continually focused on developing technology solutions adapted to our client's needs."
                },
                {
                    icon: "fas fa-temperature-low",
                    title: "Reefer Cargo",
                    text: "Regular and frequent monitoring from the receipt of the loaded container to final destination."
                },
                {
                    icon: "fas fa-boxes",
                    title: "Dry Cargo",
                    text: "We work with most types of dry cargo, from valuable cargo to the most dangerous requiring care."
                }
            ],
            procedure: [
                {
                    number: "01",
                    name: "Collection of information",
                    text: "Lorem ipsum dolor sit amet consectetur."
                },
                {
                    number: "02",
                    name: "Service Invoice Sending",
                    text: "Lorem ipsum dolor sit amet consectetur."
                },
                {
                    number: "03",
                    name: "Withdrawal of Cargo",
                    text: "Lorem ipsum dolor sit amet consectetur."
                },
                {
                    number: "04",
                    name: "Transport Customer Order",
                    text: "Lorem ipsum dolor sit amet consectetur."
                },
                {
                    number: "05",
                    name: "Successfull Delivery",
                    text: "Lorem ipsum dolor sit amet consectetur."
                }
            ],
            stats: [
                {
                    number: "128",
                    what: "Certifications"
                },
                {
                    number: "230",
                    what: "Employees"
                },
                {
                    number: "517",
                    what: "Customers"
                },
                {
                    number: "94",
                    what: "Countries Served"
                }
            ],
            feedbacks: [
                {
                    logoUrl: "logo-1",
                    text1: "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.",
                    text2: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
                },
                {
                    logoUrl: "logo-2",
                    text1: "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.",
                    text2: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."                    
                },
                {
                    logoUrl: "logo-3",
                    text1: "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.",
                    text2: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."                    
                }
            ]
        }
    },
    components: {
        TransportSection,
        Services,
        Stats,
        Feedbacks
    }
}
</script>

<style lang="scss" scoped>
    section {
        padding: 140px 0;

        &.dark_back {
            background-color: #111117;
            color: white;
        }
        &.img_back {
            background-image: url("../assets/img/bg-10.jpg");
            background-position: center;
            background-size: cover;
            color: white;
        }
    }
</style>