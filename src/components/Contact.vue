<template>
    <div class="container">
        <div class="row">
            <div class="col-8">
                <h4 class="pre_title">Send a message</h4>
                <h2 class="title">Get in <span>Touch</span></h2>
                <p>We will respond to your message as soon as possible.</p>
                <form>
                    <div class="row">
                        <div class="col-6">
                            <input type="text" placeholder="Name">
                        </div>
                        <div class="col-6">
                            <input type="text" placeholder="Email">
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-6">
                            <input type="text" placeholder="Phone">
                        </div>
                        <div class="col-6">
                            <input type="text" placeholder="More Info">
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-12">
                            <textarea placeholder="Message" rows="5"></textarea>
                        </div>
                    </div>
                    <button class="full_btn">send</button>
                </form>
            </div>
            <div class="col-4">

            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Contact",
    props: {
        info: Object
    }
}
</script>

<style lang="scss" scoped>
    .title {
        span {
            padding: 5px 15px;
            background-color: #daeced;
            color: #058283;
            border-radius: 5px;
        }
    }

    p {
        opacity: 0.5;
    }

    input {
        width: 100%;
        margin-bottom: 20px;
        background-color: #ececec;
        border: transparent;
        padding: 10px;
        border-radius: 5px;
    }

    textarea {
        width: 100%;
        background-color: #ececec;
        border: transparent;
        padding: 10px;
        border-radius: 5px;
    }

    button {
        margin-top: 50px;
    }
</style>