<template>
    <div class="container">
        <h4 class="pre_title">Road transport</h4>
        <h2 class="title">Main <span>Services</span></h2>
        <div class="d-flex justify-content-between align-items-start parag">
            <p>With all of expertise and capability comes an unrivalled commitment to customer services. We will work hard to understand your needs in order to develop a productive, long-term partnership.</p>
            <a href="#" class="empty_btn">See all</a>
        </div>
        <div class="row">
            <div class="col-4" v-for="(service, index) in services" :key="index">
                <ServiceCard :item="service" />
            </div>
        </div>
    </div>
</template>

<script>
import ServiceCard from './ServiceCard.vue'

export default {
    name: "Services",
    props: {
        services: Array
    },
    components: {
        ServiceCard
    }
}
</script>

<style lang="scss" scoped>
    .title {
        span {
            padding: 5px 15px;
            background-color: #0e272d;
            border-radius: 5px;
        }
    }

    p {
        opacity: 0.5;
    }

    .parag {
        margin-bottom: 20px;
        p {
            width: 60%;
        }
    }
</style>