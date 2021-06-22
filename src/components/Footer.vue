<template>
    <footer>
        <div class="footer_top container-fluid">
            <div class="container">
                <div class="row d-flex align-items-center box_container">
                    <div class="col-3 d-flex flex-column justify-content-between align-items-start box_footer">
                        <div class="logo"><span class="logo_text">N E X</span> G E N</div>
                        <div class="info_footer">
                            <p>A Functional HTML Template for Corporate & Business.</p>
                            <ul class="list_none">
                                <li><i class="fas fa-phone-alt"></i>{{info.phone}}</li>
                                <li><i class="fas fa-envelope"></i>{{info.mail}}</li>
                                <li><i class="fas fa-map-marker-alt"></i>{{info.location}}</li>
                            </ul>
                        </div>
                        <a href="#" class="empty_btn">Get in Touch</a>
                    </div>
                    <div v-for="(section, index) in footerLinks" :key="index" class="col-3">
                        <FooterCard :item="section"/>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer_bottom container-fluid">
            <div class="container d-flex justify-content-between align-items-center">
                <p>Enjoy the low price. We are tracking any intention of piracy</p>
                <p>&copy; 2020 NEXGEN is Proudly Powered by <a href="#">Codings</a>.</p>
            </div>
        </div>
    </footer>
</template>

<script>
import FooterCard from './FooterCard.vue'

export default {
    name: "Footer",
    props: {
        footerLinks: Array,
        info: Object
    },
    components: {
        FooterCard
    }
}
</script>

<style lang="scss" scoped>
    footer {
        color: white;

        .footer_top {
            background-color: #111117;

            .box_container {
                height: 600px;

                .box_footer {
                    height: 335px;
                    padding: 20px;

                    .info_footer {
                        opacity: 0.5;

                        ul {
                            li {
                                line-height: 30px;
                                i {
                                    margin-right: 10px;
                                }
                            }
                        }
                    }
                }
            }
        }
        .footer_bottom {
            background-color: #0d0d11;

            div {
                height: 80px;
                p {
                    margin: 0;
                }
            }
        }
    }
</style>