<template>
    <!-- Header !-->
    <div class="title">
        <h1><b>Awesome Statistics</b><br></h1>
        <p>All statistics in one place!</p>
    </div>

    </template>

    <script>
        export default {
            name:"Stats"
        }
    </script>


    <style scoped>
        @font-face {
            src:url('/src/assets/fonts/glacialindifference-regular-webfont.ttf');
            font-family: glacial;
        }
        @font-face {
            src:url('/src/assets/fonts/glacialindifference-bold-webfont.ttf');
            font-family: bglacial;
        }
        p{
            font-family: glacial;
        }
        b{
            font-family: bglacial;
        }
        .title {
            margin-left: 40%;
            width: 40%;
            vertical-align: middle;
            padding-top: 50px;
        }
    </style>

