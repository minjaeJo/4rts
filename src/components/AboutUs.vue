<template>
    <div id="about-us" class="app-frame">
        <div class="app-toolbar">
            <ul class="app-controls">
                <li class="close" @click="$emit('closeBtn')"></li>
                <li class="minimise"></li>
                <li class="maximise"></li>
            </ul>
            <div class="app-title">포트폴리오 제목</div>
        </div>
        <div class="app-body">
                    ___
                   /\__\         _____
                  /:/ _/_       /: :\  \                   Erik Bernacchi
                 /:/ /\__\     /:/\ :\  \                  Head of UX, Design & Motion
                /:/ /:/ _/_   /:/ /: :\__\
               /:/_/:/ /\__\ /:/_/:/\:|__|                 eeerik.com
               \:\/:/ /:/  / \:\/:/ /:/  /                 erik.bernacchi@gmail.com
                \::/_/:/  /   \::/_/:/  /                  +61 435 273 727
                 \:\/:/  /     \:\/:/  /
                  \::/  /       \::/  /                    ☟ Sydney, Australia
                   \/__/         \/__/


            +------------------------------------------------------------------+
            | o o o ===================== Profile.txt =========================|
            +------------------------------------------------------------------+/
            |    _      ____   ____    _ ____  _______  _ __  ___              |/
            |   | | /| / / /  / __ \  (_) __/ / __/ _ \(_) /_/__ \             |/
            |   | |/ |/ / _ \/ /_/ / / /\ \  / _// , _/ /  '_//__/       +---------------+
            |   |__/|__/_//_/\____/ /_/___/ /___/_/|_/_/_/\_\(_)         | o o o ========|
            |                                                            |---------------+/
            +------------------------------------------------------------|  more at      |/
            |                                                            | .-----------. |/
            |   Erik is a polymath mind whose areas of wizardry          |(  eeerik.com )|/
            |   range from UX, Design, Art Direction, Animation, 3D      | `-----------' |/
            |   and Programming.                                         +---------------+/
            |                                                             /////////////////
            |   Wildly obsessed with good ideas, art and softwares,       /////////////////
            |   Erik has an innate attitude to stretch the boundaries          |/
            |   and challenge the benchmarks.                                  |/
            |                                                                  |/
            |   Originally born in Italy, he now lives and works in Sydney     |/
            |   as Head of UX, Design & Motion at Traffik, Clemenger BBDO.     |/
            |                                                                  |/
            +------------------------------------------------------------------+/
            ////////////////////////////////////////////////////////////////////
            ////////////////////////////////////////////////////////////////////




                    _  _____  _______  _ _____  ___________
                ___ | |/_/ _ \/ __/ _ \(_) __/ |/ / ___/ __/
                / -_)>  </ ___/ _// , _/ / _//    / /__/ _/
                \__/_/|_/_/  /___/_/|_/_/___/_/|_/\___/___/




            ✏︎    HEAD of UX, DESIGN & MOTION - Traffik, Clemenger BBDO, Sydney
            |    Jan, 2018 —> Present
            |
            |    Leading the UX, Product Design and Motion team for cutting edge
            |    experiences, products and advertising campaigns.
            |
            |    ® Clients: Metricon, Shell, Tim Tam, Cadbury, Oreo, California Tourism
            |
            |
            |    .......................................................................
            |
            |
            ✏︎    LEAD EXPERIENCE DESIGNER - Traffik, Clemenger BBDO, Sydney
            |    Dec, 2016 —> Jan, 2018
            |
            |    UX, Product Design and Motion lead for award winning experiences,
            |    products and advertising campaigns.
            |
            |    ® Clients: Metricon, Reece, Colgate, eBay, Lendlease, V Energy, JNTO
            |
            |
            |    .......................................................................
            |
            |
            ✏︎    SENIOR DIGITAL DESIGNER - Traffik, Clemenger BBDO, Sydney
            |    Dec, 2014 —> Dec, 2016
            |
            |    Worked closely with ECD and Digital Director on experiential
            |    and advertising campaigns.
            |
            |    ® Clients: Samsung, Mazda, DHL, Mountain Dew, Schweppes, Cathay Pacific
            |
            |
            |    .......................................................................
            |
            |
            ✏︎    DIGITAL DESIGNER - McCorkell & Associates, Sydney
            |    Aug, 2013 —> Dec, 2014
            |
            |    Responsible for the production and design of digital advertising,
            |    including websites, mircosites, eDMs, banners and mobile applications.
            |
            |    ® Clients: VMware, Motorola, PayPal, AIG, LinkedIn, Navman Wireless
            |
            |
            |    .......................................................................
            |
            |
            ✏︎    DIGITAL ART DIRECTOR - Fluid, Milan
            |    May, 2008 —> Jul 2013
            |
            |    Worked closely with the Creative Director on Advertising, Graphic
            |    Design, Animation shorts, Packaging, Video, 3D rendering, Illustration
            |    and UI Design.
            |
            |    ® Clients: Jvc, Lambretta, McCain, Famosa, Spumador, Chewits
            |
            |
            ■
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
    padding: 20px;
}
</style>