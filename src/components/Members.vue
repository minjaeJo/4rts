<template>
    <div id="about-us" class="app-frame">
        <div class="app-toolbar">
            <ul class="app-controls">
                <li class="close" @click="$emit('closeBtn')"></li>
                <li class="minimise"></li>
                <li class="maximise"></li>
            </ul>
            <div class="app-title">MEMBERS</div>
        </div>
        <div class="app-body">
            <img class="profile-img" src="/static/images/profiles/jinhyuk.jpeg">
            <img class="profile-img" src="/static/images/profiles/minjae.jpeg">
            <img class="profile-img" src="/static/images/profiles/hanbin.jpeg">
            <img class="profile-img" src="/static/images/profiles/heedeok.jpeg">
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
        }
    },
    methods: {

    }
}
</script>

<style lang="scss" scoped>
#about-us {
    top:25%;
    left:25%;
    z-index:1005;
    opacity:1;
}
.app-body {
    width: 744px;
    height: 490px;
    overflow-y: scroll;
    background: #1e1e1e;
    color: #bebebe;
    text-align: center;
    .profile-img {
        display: inline-block;
        width: 200px;
        height: 200px;
        object-fit: cover;
        object-position: top;
        border-radius: 50%;
        margin: 20px 55px;
    }
}
</style>