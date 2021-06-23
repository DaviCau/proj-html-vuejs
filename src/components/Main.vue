<template>
    <main>
        <section class="transport">
            
        </section>
        <section class="dark_back services">

        </section>
        <section class="procedure">

        </section>
        <section class="img_back stats">

        </section>
        <section class="dark_back feedbacks">
            
        </section>
        <section class="contact">

        </section>
    </main>
</template>

<script>
export default {
    name: "Main",
    data() {
        return {
            vehicleTypes: [
                {
                    imgUrl: "../assets/img/truck-1.png",
                    type: "Light",
                    maxWeight: "1200"
                },
                {
                    imgUrl: "../assets/img/truck-1.png",
                    type: "Medium",
                    maxWeight: "6000"
                },
                {
                    imgUrl: "../assets/img/truck-1.png",
                    type: "Heavy",
                    maxWeight: "24000"
                }
            ],
            sevices: [
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
                    logoUrl: "../assets/img/logo-1.png",
                    text: `Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit.`
                },
                {
                    logoUrl: "../assets/img/logo-2.png",
                    text: `Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit.`                    
                },
                {
                    logoUrl: "../assets/img/logo-3.png",
                    text: `Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit.`                    
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    section {
        padding: 110px 0;

        &.dark_back {
            background-color: #111117;
            color: white;
        }
        &.img_back {
            background-image: url("../assets/img/bg-10.jpg");
            background-position: center;
            background-size: cover;
        }
    }
</style>