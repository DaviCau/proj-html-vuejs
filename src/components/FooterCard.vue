<template>
    <div class="link_section">
        <ul class="list_none">
            <li><strong>{{item.section}}</strong></li>
            <li v-for="(link, index) in item.links" :key="index"><a :href="link.url"><i class="fas fa-chevron-right"></i>{{link.text}}</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "FooterCard",
    props: {
        item: Object
    }
}
</script>

<style lang="scss" scoped>
    .link_section {
        background-color: #19191f;
        padding: 35px;
        border-radius: 10px;

        li {
            line-height: 35px;

            &:first-child {
                font-size: 24px;
                margin-bottom: 20px;
            }
        
            a {
                color: rgba($color: #ffffff, $alpha: 0.5);
                text-decoration: none;
                
                i {
                    margin-right: 10px;
                }
            }
        }
    }
</style>