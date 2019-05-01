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
        <div v-if="!target_project.open" class="app-body">
            <div class="project-card" v-for="(project, index) in projects" :key="index" @click="touchProject(project)">
                <img class="project-img" :src="project.gif">
                <div class="project-title">{{project.title}}</div>
            </div>
        </div>
        <div v-else class="app-body project-description" v-html="target_project.content"></div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            projects: [
                {
                    title: "The Internet is for Porn",
                    gif: "/static/images/this_is_the_internet.gif",
                    content: "<div>인터넷이란 거대 네트워크의 형성은 수많은 정보의 공유와 콘텐츠의 개발을 가능토록 했습니다. 그 발전 양상은 비약적이고 광범위한 동시에 점차 분산적이고 개별적인 모습을 보였으며, 수없이 상업화되고 다양화된 욕망의 군집체는 거대한 모노리스가 되었습니다. 그중에서도 가장 원초적인 욕구와 자극을 바탕으로 성장한 포르노는, 그 안에서 쉬이 드러낼 수 없지만 절대 묵과할 수 없는 권력을 지니고 있습니다.</div>"
                            +"<div> 작품은 포르노의 매개가 되는 인터넷 사이트가, 그 주체와 마찬가지로 '합의되지 않은' 방식의 광고와 강제적 이동을 통해 포르노의 재상산에 일조한다는 점에 초점을 두었습니다. 우리는 필요로 하는 정보를 얻기 위해서 필요로 하지 않는 더 많은 것들을 마주해야만 합니다. 그렇기에 규제될 수 없는 방식으로 범람하는 포르노들은 그것이 소비되는 만큼 ‘익명’ 하 피해자들뿐만 아니라 미필적인 가해자를 재생산합니다. 특히 자극만을 좇는 왜곡된 성적 묘사와 비윤리적이고 범법적인 유통방식에 대한 묵시적 순응은 결국 인터넷을 ‘포르노를 찾기 위한 공간(used for porn)’을 넘어 ‘포르노가 존재하기 위한(exists for porn)’ 것으로 전치하고 말 것입니다.</div>"
                            +"<div> 이런 실태를 희화화하고 시각적으로 재구성함으로써 이에 대한 경각심을 환기하고 구조적인 문제를 제기하는 것이 작품의 기획 의도입니다. 관람객들이 검색 플랫폼에 무엇을 검색하든 기존에 찾던 정보는 해체되고 화면에는 선정적인 이미지를 표상하는 각종 Meme들이 난무합니다. 단계적으로 심화되는 시각화 과정을 통해 관람객들은 유사 포르노사이트들의 암시 효과를 받을 수 있으며, 강제적이고 합의가 배제된 채 욕구가 소비되는 방식적 모순을 작품 밖의 경험으로 끌어내어 객관화하는 기회를 가질 수 있습니다.</div>"
                            +"<a href='https://www.minjae.dev/TheInternetIsForPorn/'>Web_Link: The Internet is for the Porn</a>"
                },
                {
                    title: "The Internet is for Porn2",
                    gif: "/static/images/this_is_the_internet.gif",
                    content: "인터넷이란체되고 선정적인 이미지를 표상하는 각종 Meme들이 난무하게 됩니다. 단계적으로 심화되는 시각화 과정을 통해 관람객들은 유사 포르노사이트들의 암시 효과를 받을 수 있으며, 강제적이고 합의가 배제된 채 욕구가 소비되는 방식적 모순을 작품 밖의 경험으로 끌어내어 객관화하는 기회를 갖게 됩니다. "
                },
                {
                    title: "The Internet is for Porn3",
                    gif: "/static/images/this_is_the_internet.gif",
                    content: "인터넷이란 거대 네트워크의 형성은 수많은 정보의 공유와 게 됩니다. "
                },
                {
                    title: "The Internet is for Porn4",
                    gif: "/static/images/this_is_the_internet.gif",
                    content: "인터넷이란 거대 네트워크의 형다. "
                },
                {
                    title: "The Internet is for Porn5",
                    gif: "/static/images/this_is_the_internet.gif",
                    content: "인터넷이란 거대 네트워크의 형성은 수많은 정보의 공유와 콘텐츠의 개발을 가능토록 했습니다."
                },
                {
                    title: "The Internet is for Porn6",
                    gif: "/static/images/this_is_the_internet.gif",
                    content: "인터넷이란"
                }
            ],
            target_project: {
                open: false,
                content: ''
            }
        }
    },
    methods: {
        touchProject(project) {
            console.log(project)
            this.target_project.open = true;
            this.target_project.content = project.content;
        }
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
    .project-card {
        width:250px;
        text-align: center;
        margin: 45px 50px;
            .project-img {
                width:250px;
            }
            .project-title {
                font-size: 15px;
                margin-top: 10px;
            }
    }
}
.project-description {
    padding: 15px;
    text-indent: 10px;
    letter-spacing: 1.6px;
    font-size: 14px;
}
</style>