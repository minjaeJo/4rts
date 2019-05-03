<template>
    <div id="contact" class="app-frame">
        <div class="app-toolbar">
            <ul class="app-controls">
                <li class="close" @click="$emit('closeBtn')"></li>
                <li class="minimise"></li>
                <li class="maximise"></li>
            </ul>
            <div class="app-title">Contact</div>
        </div>
        <div class="app-body">
            <div class="contact-block">
                <img src="/static/images/front_contact_us.png">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            email: '',
            title: '',
            context: ''
        }
    },
    methods: {

    }
}
</script>

<style lang="scss" scoped>
#contact {
    top:25%;
    left:25%;
    z-index:1005;
    opacity:1;
}
.app-body {
    width: 600px;
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    overflow-y: scroll;
    box-sizing: border-box;
    justify-content: center;
    background: #1e1e1e;
    color: #bebebe;
    .title {
        margin-top: 40px;
        font-weight: 700;
        font-size: 40px;
        margin-bottom: 13px;
    }
}
.form-format {
    margin: 0px 20px;
}
.contact-block {
    img {
        width: 600px;
        height: 338px;
    }
}
@media only screen and (max-width: 880px) {
    .contact-block {
        margin-top: 25vh;
        img {
            width: 100%;
            height: auto;
            align-items: center;
        }
    }
}

</style>