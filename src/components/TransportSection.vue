<template>
    <div class="container transport_section">
        <div class="row">
            <div class="col-8 left_side">
                <h4 class="pre_title">Who we are</h4>
                <h2 class="title"><span><i class="far fa-gem"></i> Excellence</span> in Transport</h2>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab a sequi dignissimos fuga veniam perspiciatis optio nisi neque obcaecati natus aperiam consequuntur nihil odit quia delectus quae dolore magnam.
                </p>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis, quia velit minus, quae officia esse id asperiores aliquid corporis aliquam vel harum quibusdam, culpa nemo.
                </p>
                <p class="border_left">
                    <em>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Animi, quis earum. Ex quaerat rem quo libero facere accusantium facilis neque. Perferendis repellat quis quas.</em>
                </p>
                <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Harum, eos.</p>
                <ul>
                    <li><p>Lorem ipsum dolor sit amet.</p></li>
                    <li><p>Lorem, ipsum dolor.</p></li>
                    <li><p>Lorem ipsum dolor sit.</p></li>
                    <li><p>Lorem ipsum dolor sit amet consectetur.</p></li>
                    <li><p>Lorem ipsum dolor sit.</p></li>
                </ul>
            </div>
            <aside class="col-4">
                <div class="vehicles">
                    <h3>Vehicles</h3>
                    <div v-for="(vehicle, index) in vehicles" :key="index" class="d-flex">
                        <img :src="require(`../assets/img/${vehicle.imgUrl}.png`)" alt="truck">
                        <div class="type">
                            <h3>{{vehicle.type}}</h3>
                            <p>Max Weight {{vehicle.maxWeight}} Kg</p>
                        </div>
                    </div>
                </div>
                <h3>Certifications</h3>
                <div class="d-flex justify-content-between certifications">
                    <img src="../assets/img/certificate.png" alt="certificate">
                    <img src="../assets/img/certificate.png" alt="certificate">
                </div>
            </aside>
        </div>
    </div>
</template>

<script>
export default {
    name: "TransportSection",
    props: {
        vehicles: Array
    }
}
</script>

<style lang="scss" scoped>
.transport_section{
    color: #21333e;

    p {
        opacity: 0.5;
    }

    .left_side {

        .title {
            
            span {
                padding: 5px 15px;
                background-color: #daeced;
                color: #058283;
                border-radius: 5px;
            }
        }

        .border_left {
            border-left: solid 5px #daeced;
            padding: 20px;
        }

        ul {
            padding-left: 20px;

            p {
                margin: 0;
                line-height: 25px;
            }
        }
    }

    aside {
        padding: 0 30px;

        h3 {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 15px;
        }

        .vehicles {
            padding-bottom: 30px;

            img {
                height: 70px;
                background-color: #daeced;
                padding: 5px;
                margin-right: 20px;
                border-radius: 5px;
            }
        }

        .certifications {
            width: 100%;
            img {
                height: 150px;
            }
        }
    }
}
</style>