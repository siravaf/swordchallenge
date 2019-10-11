<template>

    <div class="row header">

        <div class="col-md-4">
            <img class="logo" alt="logo"  src="@/assets/images/SWORD_Health_logo.svg" >
        </div>
        <div class="col-md-4"></div>
        <div class="col-md-4 title">
        <b>Frontend Developer</b><br>
            Challenge
        </div>
    </div>

</template>

<script>
    export default {
        name: "Header"
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
    .header {

        background: #D8D8D8;
        height: 80px;
        left: 0;
        right: 0;
        top: 0;

    }

    .logo {
        margin-left: 50%;
        margin-top: 5%;
        width: auto;
        height: 30px;
    }

    .title {
        margin-top: 15px;
    }
</style>