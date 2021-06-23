<template>
    <div class="d-flex flex-column align-items-start">
        <img class="logo" :src="require(`../assets/img/${item.logoUrl}.png`)" alt="logo">
        <p>{{item.text1}}</p>
        <p>{{item.text2}}</p>
    </div>
</template>

<script>
export default {
    name: "FeedbackCard",
    props: {
        item: Object
    }
}
</script>

<style lang="scss" scoped>
    div {
        padding: 40px;
        background-color: #19191f;
        border-radius: 10px;
        position: relative;

        span {
            position: absolute;
            bottom: 15px;
            right: 20px;
        }

        .logo {
            height: 30px;
            filter: invert(1);
            margin-bottom: 20px;
        }
        p {
            opacity: .5;
        }
    }
</style>