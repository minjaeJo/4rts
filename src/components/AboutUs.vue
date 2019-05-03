<template>
    <div id="about-us" class="app-frame">
        <div class="app-toolbar">
            <ul class="app-controls">
                <li class="close" @click="$emit('closeBtn')"></li>
                <li class="minimise"></li>
                <li class="maximise"></li>
            </ul>
            <div class="app-title">ABOUT US</div>
        </div>
        <div class="app-body">
            <p><span style="font-weight: 700; font-size: 17px">4rts</span>는 예술을 두고 마음이 맞는 4명이 함께 모인, 친구이자 조직입니다.</p>
            <p class="text">‘Arts’의 모습으로 보이기도 하고, ‘예술을 위하여(for Arts)’를 뜻하는 영어 발음으로 읽히기도 하는 4rts(포아츠)라는 이름과 같이, 저희는 예술적인 것에 끊임없이 관심을 가지고 함께 하고자 합니다.
            <p class="text">예술을 위한다는 말에는 예술적인 것을 찾기 위한다는(lookin’ for art) 의미와, 예술이 되고자 필요한 것들을 갖춰나간다는(get something for art) 두 의미가 모두 함축되어 있습니다. 멋지고 즐거움을 주는 것들부터, 의미와 가치를 담아낸 것들에 이르기까지, 당장 하고 싶은 일들과 갖추고 있는 능력을 바탕으로 새로운 것을 도전하고 찾아 나설 것입니다.</p>
            <p>하던 일도, 가지고 있던 생각도 모두 다르지만, 그렇기에 기술, 학문, 문화, 서로가 발 딛고 있는 위치에서 바라보는 풍경들을 나눌 수 있습니다. 이를 함께 멋지게 표현하고 싶은, 때론 새로운 시선으로 함께 그림을 그리고 싶은 분들이라면, 언제나 맞이할 준비가 되어있습니다. 환영합니다.</p>
            <div>Spread4rts.com</div>
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
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    overflow-y: scroll;
    box-sizing: border-box;
    justify-content: center;
    background: #1e1e1e;
    color: #bebebe;
    white-space: pre-wrap;
    word-wrap: break-word;
    font-size: 14px;
    letter-spacing: 2px;
    padding: 45px;
    .text {
        text-indent: 10px;
        margin-bottom: 0px;
    }
    div {
        color: #e6362b;
        font-size: 20px;
    }
}
</style>