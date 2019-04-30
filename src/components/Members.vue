<template>
    <div id="members" class="app-frame">
        <div class="app-toolbar">
            <ul class="app-controls">
                <li class="close" @click="$emit('closeBtn')"></li>
                <li class="minimise"></li>
                <li class="maximise"></li>
            </ul>
            <div class="app-title">MEMBERS</div>
        </div>
        <div class="app-body">
            <div class="profile-descript">
                <span>Touch Picture</span>
                <img src="/static/images/touch_picture.png">
            </div>
            <div id="jinhyuk" class="profile-container" @click="touchPicture">
                <img class="profile-img" src="/static/images/profiles/jinhyuk.jpeg">
                <div class="profile-text">
                    <b>정진혁</b><br><br>
                    #중앙대학교 융합공학부<br>
                    #IT 헤드헌터 네트워크<br>
                    #ᄆᄉ 아트 그룹 PM<br>
                    #2014대한민국 발명 장학생<br>
                </div>
            </div>
            <div id="hanbin" class="profile-container" @click="touchPicture">
                <img class="profile-img" src="/static/images/profiles/hanbin.jpeg">
                <div class="profile-text">
                    <b>박한빈</b><br><br>
                    #서울대학교 자유전공학부<br>
                    #서울대학교 대표 입학컨설턴트<br>
                    #NHN 웹 메거진 에디터<br>
                    #Young SAMSUNG 8기<br>
                </div>
            </div>
            <div id="minjae" class="profile-container" @click="touchPicture">
                <img class="profile-img" src="/static/images/profiles/minjae.jpeg">
                <div class="profile-text">
                    <b>조민재</b><br><br>
                    #서울시립대 컴퓨터과학과<br>
                    #Microsoft Student Partner<br>
                    #BOAZ 빅데이터 시각화 담당<br>
                    #FrontEnd(WEB,iOS)<br>
                </div>
            </div>
            <div id="heedeok" class="profile-container" @click="touchPicture">
                <img class="profile-img" src="/static/images/profiles/heedeok.jpeg">
                <div class="profile-text">
                    <b>손희덕</b><br><br>
                    #중앙대학교 전기전자공학부<br>
                    #AI Curation Engine 담당<br>
                    #iOS Programming 프리랜서<br>
                    #AR 컨텐츠 개발 프리랜서<br>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            prev_target: ''
        }
    },
    methods: {
        touchPicture(event) {
            const target = $(event.target.parentNode).attr('id');
            if(this.prev_target) {
                $('#'+this.prev_target+' .profile-text').css('visibility','hidden');
            }
            $('#'+target+' .profile-text').css('visibility','visible');
            this.prev_target = target;
        }
    }
}
</script>

<style lang="scss" scoped>
#members {
    top:25%;
    left:25%;
    z-index:1005;
    opacity:1;
}
.app-body {
    width: 744px;
    height: 535px;
    overflow-y: scroll;
    background: #1e1e1e;
    color: #bebebe;
    text-align: center;
    .profile-descript {
        text-align: left;
        margin: 15px 0 0 15px;
        font-size: 16px;
        font-weight: 700;
        span {
            vertical-align: middle;
        }
        img {
            width: 25px;
            margin-left: 5px;
        }
    }
    .profile-container {
        position: relative;
        display: inline-block;
        width: 200px;
        height: 200px;
        margin: 20px 55px;
        .profile-img {
            width: 200px;
            height: 200px;
            object-fit: cover;
            object-position: top;
            border-radius: 50%;
        }
        .profile-text {
            visibility: hidden;
            position: absolute;
            top:0%;
            width: 200px;
            height: 200px;
            z-index: 1500;
            background: rgba(0,0,0,0.75);
            border-radius: 100px;
            font-size: 14px;
            padding-top:32px;

        }
    }
}
</style>