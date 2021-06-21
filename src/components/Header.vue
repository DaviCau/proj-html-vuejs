<template>
    <header>
        <div class="container-fluid info_container">
            <div class="container d-flex justify-content-between align-items-center info">
                <div>
                    <i class="fas fa-clock"></i> <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
                </div>
                <div>
                    <ul class="d-flex list_none">
                        <li><i class="fas fa-phone-alt"></i> <span>+1 (305) 1234-5678</span></li>
                        <li><i class="fas fa-envelope"></i> <span>hello@example.com</span></li>
                        <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
                        <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                        <li><a href="#"><i class="fab fa-linkedin-in"></i></a></li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="jumbotron">
            <div class="back_jumbo container-fluid">
                <div class="container">
                    <nav class="d-flex justify-content-between align-items-center">
                        <div class="nav_left"><span>N E X</span> G E N</div>
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
    }
}
</script>

<style lang="scss" scoped>
    .info_container {
        background-color: #21333e;
        color: white;

        .info {
            height: 50px;

            ul {
                
                li {
                    margin-left: 20px;

                    a {
                        color: white;
                    }
                }
            }
        }
    }

    .jumbotron {
        background-image: url(../assets/img/bg-9.jpg);
        background-position-x: center;

        .back_jumbo {
            background-color: rgba(0, 0, 0, 0.5);
            height: 870px;

            nav {
                height: 80px;
            
                .nav_left {
                    color: white;
                    font-weight: bold;
                    span {
                        color: #00a6a6;
                        background-color: rgba($color: #00a6a6, $alpha: 0.2);
                        padding: 10px 5px 10px 25px;
                        border-top-left-radius: 20px;
                        border-bottom-left-radius: 20px;
                    }
                }
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
        }
    }
</style>