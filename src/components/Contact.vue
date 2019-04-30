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
            <div class="title">Contact Us</div>
            <b-form-input class="form-format" v-model="name" placeholder="이름"></b-form-input>
            <b-form-input class="form-format" v-model="email" placeholder="E-Mail"></b-form-input>
            <b-form-input class="form-format" v-model="title" placeholder="제목"></b-form-input>
            <b-form-textarea class="form-format" v-model="context" placeholder="내용" :rows="8" :max-rows="8"></b-form-textarea>
            <b-btn variant="gradation-gray">제출</b-btn>
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
    width: 744px;
    height: 490px;
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
</style>