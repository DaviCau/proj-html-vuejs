<template>
    <div class="container text-center">
        <h4 class="pre_title">what are we doing</h4>
        <h2 class="title"><span>Results</span> in Numbers</h2>
        <div class="d-flex justify-content-around stats_container">
            <div v-for="(info, index) in stats" :key="index">
                <div class="number">{{info.number}}</div>
                <div class="what">{{info.what}}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Stats",
    props: {
        stats: Array
    }
}
</script>

<style lang="scss" scoped>
    .title {
        span {
            padding: 5px 15px;
            background-color: rgba($color: #018385, $alpha: 0.3);
            border-radius: 5px;
        }
    }

    .stats_container {
        margin-top: 140px;
        font-weight: bold;
        .number {
            font-size: 40px;
            color: #00a6a6;
            margin-bottom: 20px;
        }
        .what {
            font-size: 28px;
        }
    }
</style>