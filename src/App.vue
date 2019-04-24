<template>
    <div id="app">
        <boot></boot>
        <div>
            <header>
                <navigation></navigation>
            </header>
            <content>
                <div id="windows">
                    <div v-if="is_portfolio" class="app-frame" style="top:197px;left:218px;z-index:1005;opacity:1;">
                        <div class="app-toolbar">
                            <ul class="app-controls">
                                <li class="close" @click="is_portfolio = false"></li>
                                <li class="minimise"></li>
                                <li class="maximise"></li>
                            </ul>
                            <div class="app-title">포트폴리오 제목</div>
                        </div>
                        <div class="app-body-template" style="width: 744px;height: 490px;"></div>
                    </div>
                </div>
                <div id="files">
                    <div class="file" @click="is_portfolio = true">
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
            is_portfolio: false
        }
    },
    methods: {

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
    background: #f81518;
}
#windows {
    .app-frame {
        position: absolute;
        top: 0px;
        left: 0px;
        z-index: 10;
        -webkit-box-shadow: 0 35px 36px rgba(255, 0, 0, 0.1);
        -moz-box-shadow: 0 35px 36px rgba(255, 0, 0, 0.1);
        box-shadow: 0 35px 36px rgba(255, 0, 0, 0.1);
        /* visibility: hidden; */
        .app-toolbar {
            position: absolute;
            background-color: #202020;
            border-radius: 3px;
            width: 100%;
            height: 20px;
            display: flex;
            justify-content: center;
            /* background-image: url(../img/details/DoubleLine.png); */
            background-repeat: repeat-x;
            background-position-y: center;
            li {
                width: 12px;
                height: 12px;
                float: left;
                margin: 4px 0;
                margin-left: 7px;
                border-radius: 25px;
                list-style-type: none;
                cursor: pointer;
            }
            .app-controls {
                position: absolute;
                left: 0;
                margin: 0;
                padding: 0;
                .close {
                    background: #ff5953;
                }
                .minimise {
                    background: #e6c029;
                }
                .maximise {
                    background: #53c22b;
                }
            }
        }
        .app-title {
            text-align: center;
            font-size: 13px;
            line-height: 16px;
            letter-spacing: 2.5px;
            padding: 2px 15px;
            color: #bdbebe;
        }
        .app-body-template {
            display: flex;
            flex-wrap: wrap;
            align-items: flex-start;
            overflow-y: scroll;
            padding-top: 50px;
            padding-bottom: 20px;
            box-sizing: border-box;
            justify-content: center;
            background: #1e1e1e;
        }
    }
}
#files {
    position: absolute;
    left: 10px;
    top: 60px;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: center;
    height: 90%;
    .file {
        /* position: absolute; */
        display: flex;
        flex-direction: column;
        align-items: center;
        color: #000;
        margin: 15px;
        cursor: pointer;
        .file-icon {
            margin: 10px;
            width: 70px;
            height: 70px;
            background-size: 70px 70px;
            background-image: url(https://image.flaticon.com/icons/svg/1648/1648992.svg);
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
