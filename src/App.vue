<template>
    <div id="app">
        <boot></boot>
        <div>
            <header>
                <navigation></navigation>
            </header>
            <content>
                <div id="windows"></div>
                <div id="files">
                    <div class="file">
                        <div class="file-icon"></div>
                        <div class="file-title">FILENAME</div>
                    </div>
                    <div class="file">
                        <div class="file-icon"></div>
                        <div class="file-title">FILENAME</div>
                    </div>
                    <div class="file">
                        <div class="file-icon"></div>
                        <div class="file-title">FILENAME</div>
                    </div>
                    <div class="file">
                        <div class="file-icon"></div>
                        <div class="file-title">FILENAME</div>
                    </div>
                    <div class="file">
                        <div class="file-icon"></div>
                        <div class="file-title">FILENAME</div>
                    </div>
                </div>

            </content>
        </div>
    </div>
</template>

<script>
import {TweenMax, CSSPlugin, ScrollToPlugin, Draggable} from 'gsap/all'
import Navigation from './components/Navigation'
import Boot from './components/Boot'
export default {
    components: {
        Navigation,
        Boot
    },
    data() {
        return {
            // is_boot: true
        }
    }
}
</script>

<style lang="scss">
    body {
        position: relative;
        width: 100vw;
        height: 100vh;
        margin: 0px;
    }
    header {
        width: 100%;
        height: 31px;
        font-size: 15px;
        background-color: #202020;
        justify-content: space-between;
    }
    content {
        width: 100%;
        height: calc(100vh - 31px);
        display: block;
        background: #0cff01
    }
    #files {
        position: absolute;
        left: 10px;
        top: 60px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        align-items: center;
        height: 80%;
        .file {
            /* position: absolute; */
            display: flex;
            flex-direction: column;
            align-items: center;
            color: var(--black);
            margin: 15px;
            cursor: pointer;
            .file-icon {
                margin: 10px;
                width: 70px;
                height: 70px;
                background-size: 70px 70px;
                background-image: url(https://github.githubassets.com/images/spinners/octocat-spinner-128.gif);
            }
            .file-title {
                text-align: center;
                font-size: 15px;
                padding: 6px 6px 4px 6px;
                letter-spacing: 1.06px;
                line-height: 14px;
                margin-top: 3px;
            }
        }
    }
</style>
