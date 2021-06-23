<template>
    <div class="d-flex flex-column align-items-start">
        <i class="main_icon" :class="item.icon"></i>
        <h3>{{item.title}}</h3>
        <p>{{item.text}}</p>
        <i class="arrow fas fa-arrow-right"></i>
    </div>
</template>

<script>
export default {
    name: "ServiceCard",
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

        .arrow {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 25px;
            color: #0f4e51;
        }

        .main_icon {
            padding: 20px;
            font-size: 25px;
            color: #058283;
            background-color: #16282e;
            border-radius: 50%;
        }

        h3 {
            padding: 20px 0;
            font-weight: bold;
        }
        p {
            opacity: .5;
        }
    }
</style>