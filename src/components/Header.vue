<template>
    <header>
        <div class="info_container">
            <div class="container d-flex justify-content-between align-items-center py-3">
                <div>
                    <i class="fas fa-clock"></i>{{info.openingTime}}
                </div>
                <div>
                    <ul class="d-flex list_none">
                        <li><i class="fas fa-phone-alt"></i>{{info.phone}}</li>
                        <li><i class="fas fa-envelope"></i>{{info.mail}}</li>
                        <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
                        <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                        <li><a href="#"><i class="fab fa-linkedin-in"></i></a></li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="jumbotron">
            <div class="back_jumbo">
                <div class="container">
                    <nav class="d-flex justify-content-between align-items-center">
                        <div class="nav_left logo"><span>N E X</span> G E N</div>
                        <div class="nav_right">
                            <ul class="d-flex list_none">
                                <li v-for="(link, index) in navLinks" :key="index">
                                    <a class="nav_link" :href="link.url">{{link.name}}</a>
                                </li>
                                <li><a class="nav_link" href="#"><i class="far fa-user"></i></a></li>
                                <li><a class="full_btn" href="#">Get in Touch</a></li>
                            </ul>
                        </div>
                    </nav>
                    <div class="jumbotron_content">
                        <h4 class="pre_title">logistics services</h4>
                        <h1>Cargo transport</h1>
                        <p>Fractional or exclusive road cargo transportation to all regions, with small, medium and large vehicles</p>
                        <div class="jumbotron_buttons">
                            <a class="full_btn" href="#">Get in Touch</a>
                            <a class="empty_btn" href="#">Read More</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
    props: {
        navLinks: Array,
        info: Object
    }
}
</script>

<style lang="scss" scoped>
    header {
        color: white;

        .info_container {
            background-color: #21333e;
            font-size: 14px;
            color: rgba($color: #ffffff, $alpha: 0.5);

            i {
                margin-right: 10px;
            }

            ul {
                
                li {
                    margin-left: 20px;

                    a {
                        color: rgba($color: #ffffff, $alpha: 0.5);
                    }
                }
            }
        }

        .jumbotron {
            background-image: url("../assets/img/bg-9.jpg");
            background-position-x: center;
            background-size: cover;


            .back_jumbo {
                background-color: rgba(0, 0, 0, 0.5);
                height: 860px;
                position: relative;

                nav {
                    height: 80px;
                
                    .nav_right {
                        ul {
                            li {
                                margin-left: 30px;
                                color: white;
                            }

                            .nav_link {
                                text-decoration: none;
                                color: white;
                                font-weight: bold;
                                text-transform: uppercase;
                            }
                        }
                    }
                }

                .jumbotron_content {
                    position: absolute;
                    top: 50%;
                    transform: translateY(-50%);
                    width: 30%;
                    
                    h1 {
                        font-size: 80px;
                        text-transform: uppercase;
                        font-weight: bold;
                        margin: 0;
                    }
                    p {
                        font-size: 22px;
                        margin: 40px 0;
                    }
                    .jumbotron_buttons {
                        margin: 20px 0 0;
                        
                        a {
                            margin-right: 20px;
                        }
                    }
                }
            }
        }
    }
</style>