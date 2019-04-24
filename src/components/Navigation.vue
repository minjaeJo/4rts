<template>
    <div class="navigation-container">
        <div class="menu-list">
            <div class="column-header" id="portfolio-title">
                <span id="header-mainlogo"></span>
                Portfolio Name
            </div>
        </div>
        <div class="menu-list utils">
            <div class="column-header">
                File
            </div>
        </div>
        <div class="menu-list utils">
            <div class="column-header">
                View
            </div>
        </div>
        <div class="menu-list utils">
            <div class="column-header">
                Help
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
    .navigation-container {
        margin: 0;
        padding: 0;
        border: 0;
        font-size: 100%;
        font-family: inherit;
        vertical-align: baseline;
        .menu-list {
            position: relative;
            display: inline-block;
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: white;
            line-height: 18px;

            .column-header {
                padding: 7px 20px 6px 20px;
            }
            #header-mainlogo {
                position: absolute;
                left: 15px;
                top: 4px;
                width: 25px;
                height: 21px;
                display: inline-block;
                background-repeat: no-repeat;
                background-position: center;
                background-size: contain;
                background: #fff;
                border-radius: 5px;
            }
            #portfolio-title {
                /* background: var(--gradient-Straight1);
                background-size: 150% 150%;
                background-position: center; */
                padding: 7px 40px 6px 56px;
                margin-right: 20px;
            }
        }
    }
</style>