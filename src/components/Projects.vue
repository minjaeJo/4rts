<template>
    <div id="projects" class="app-frame">
        <div class="app-toolbar">
            <ul class="app-controls">
                <li class="close" @click="$emit('closeBtn')"></li>
                <li class="minimise"></li>
                <li class="maximise"></li>
            </ul>
            <div class="app-title">Projects</div>
        </div>
        <div class="app-body">

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
#projects {
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
}
</style>