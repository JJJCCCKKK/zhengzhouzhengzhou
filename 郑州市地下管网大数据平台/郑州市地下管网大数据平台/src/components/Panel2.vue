<template>
    <div class="panel">
        <div class="title">
            <slot name="header"></slot>
        </div>
        <span class="text1">管网实时水位</span>
        <div class="num">
            <slot name="number"></slot>
        </div>
        <span class="text2">m</span>
    </div>
</template>

<script setup></script>
<style scoped>
    .panel {
        background: url('../assets/方形216.png');
        width: 250px;
        height: 100px;
        background-size: 100% 100%;
        background-repeat: no-repeat;
        background-position: 24%;
        position: relative;
    }

    .panel::after {
        content: '';
        position: absolute;
        left: 0;
        top: 10px;
        width: 99%;
        height: 93%;
        background-color: #33435345;
        backdrop-filter: blur(10px);
        z-index: -1;
    }

    .title {
        font-family: 'Times New Roman', cursive;
        text-transform: uppercase;
        font-size: 19px;
        color: #cce7f8;
        position: absolute;
        left: 98px;
        top: 25px;
        width: 200px;
        margin-left: 25px;
        text-shadow: 0 0 6px rgba(182, 211, 207, 0.9),
            0 0 30px rgba(182, 211, 207, 0.3),
            0 0 12px rgba(15, 115, 223, 0.5),
            0 0 21px rgba(15, 115, 223, 0.9),
            0 0 34px rgba(15, 115, 223, 0.8),
            0 0 54px rgba(15, 115, 223, 0.9);
    }

    .num {
        background: rgba(0, 0, 0, 0);
        font-family: wgsFont;
        font-size: 30px;
        color: rgb(0, 185, 40);
        text-align: center;
        position: absolute;
        right: 56px;
        top: 50px;
        text-shadow: 0px 0px 20px rgb(96, 239, 19);
    }

    .text1 {
        background: rgba(0, 0, 0, 0);
        font-family: 'YouYuan', cursive;
        text-transform: uppercase;
        font-size: 15px;
        color: #cce7f8;
        position: absolute;
        left: 35px;
        top: 65px;
    }

    .text2 {
        background: rgba(0, 0, 0, 0);
        font-family: 'Times New Roman';
        font-size: 16px;
        color: #cce7f8;
        position: absolute;
        right: 35px;
        top: 65px;
    }

    @font-face {
        font-family: 'wgsFont';
        src: url('../assets/font/open_24_display_st-webfont.eot');
        src: url('../assets/font/open_24_display_st-webfont.eot#iefix')
                format('embedded-opentype'),
            url('../assets/font/open_24_display_st-webfont.woff2')
                format('woff2'),
            url('../assets/font/open_24_display_st-webfont.woff')
                format('woff'),
            url('../assets/font/open_24_display_st-webfont.ttf')
                format('truetype'),
            url('../assets/font/open_24_display_st-webfont.svg')
                format('svg');
    }
</style>