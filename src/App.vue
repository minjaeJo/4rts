<template>
    <div id="app">
        <boot></boot>
        <div>
            <header>
                <navigation></navigation>
            </header>
            <content>
                <div id="windows">
                    <about-us v-if="is_about_us" @closeBtn="closeBtn('aboutus')"></about-us>
                    <members v-if="is_members" @closeBtn="closeBtn('members')"></members>
                    <contact v-if="is_contact" @closeBtn="closeBtn('contact')"></contact>
                </div>
                <div id="files">
                    <div class="file" @click="closeBtn('aboutus')">
                        <div class="file-icon" style="background-image: url('/static/images/question.png')"></div>
                        <div class="file-title">ABOUT US</div>
                    </div>
                    <div class="file" @click="closeBtn('members')">
                        <div class="file-icon" style="background-image: url('/static/images/members.png')"></div>
                        <div class="file-title">MEMBERS</div>
                    </div>
                    <div class="file">
                        <div class="file-icon"></div>
                        <div class="file-title">PROJECTS</div>
                    </div>
                    <div class="file">
                        <div class="file-icon"></div>
                        <div class="file-title">PRESS</div>
                    </div>
                    <div class="file" @click="closeBtn('contact')">
                        <div class="file-icon"></div>
                        <div class="file-title">CONTACT</div>
                    </div>
                </div>
            </content>
        </div>
    </div>
</template>

<script>
import {TweenMax, CSSPlugin, ScrollToPlugin, Draggable} from 'gsap/all';
import Navigation from './components/Navigation';
import Boot from './components/Boot';
import AboutUs from './components/AboutUs';
import Members from './components/Members';
import Contact from './components/Contact'
export default {
    components: {
        Navigation,
        Boot,
        AboutUs,
        Members,
        Contact
    },
    mounted() {
    },
    data() {
        return {
            is_about_us: false,
            is_members: false,
            is_contact: false
        }
    },
    methods: {
        closeBtn(display) {
            switch (display) {
                case 'aboutus':
                    this.is_about_us = !this.is_about_us;
                    break;
                case 'members':
                    this.is_members = !this.is_members;
                case 'contact':
                    this.is_contact = !this.is_contact;
                default:
                    break;
            }
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
            background-color: #202020;
            width: 100%;
            height: 18px;
            display: flex;
            justify-content: center;
            /* background-image: url(../img/details/DoubleLine.png); */
            background-repeat: repeat-x;
            background-position-y: center;
            li {
                width: 10px;
                height: 10px;
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
            font-size: 12px;
            line-height: 15px;
            letter-spacing: 2.5px;
            padding: 2px 15px;
            color: #bdbebe;
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
