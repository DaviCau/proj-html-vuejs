<template>
    <div class="container">
        <h4 class="pre_title text-center">customer testimonials</h4>
        <h2 class="title text-center">Trusted <span>Feedback</span></h2>
        <p class="text-center">We work intensively in search of ideals that can add up in the lives of our customers. This is what moves us and we are frateful for the recognition.</p>
        <div class="row">
            <div class="col-4" v-for="(feedback, index) in feedbacks" :key="index">
                <FeedbackCard :item="feedback" />
            </div>
        </div>
    </div>
</template>

<script>
import FeedbackCard from './FeedbackCard.vue'

export default {
    name: "Feedbacks",
    props: {
        feedbacks: Array
    },
    components: {
        FeedbackCard
    }
}
</script>

<style lang="scss" scoped>
    p {
        width: 60%;
        margin: 0 auto 35px;
        opacity: 0.5;
    }
</style>