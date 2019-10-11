<template>
    <div class="gameSection">
        <!-- Header !-->
        <div class="title">
            <h1><b>Tic Tac Toe Games</b><br></h1>
            <p>Welcome to the best game in the world</p>
        </div>


        <!-- Buttons !-->

        <div class="row">
            <div class="col-md-4"></div>
            <div class="btn-group col-md-4" role="group">
                <button type="button" class="btn buttonboxSelect">Tic Tac Toe</button>
                <button type="button" class="btn buttonbox">4-in-a-row</button>
            </div>
            <div class="col-md-4"></div>
        </div>
        <br>
        <br>

        <!-- Game !-->
        <div class="row ">
            <div class="col-md-3 gameArea">
                <h1><b>Player 1</b></h1>
                <h2>2</h2>
            </div>

            <div class="col-md-6">
                <div class="box">
                <Play/>
                </div>
            </div>
            <div class="col-md-3 gameArea2">
                <h1><b>Player 2</b></h1>
                <h2>4</h2>
            </div>
        </div>
    </div>

</template>

<script>

    import Play from "@/components/layouts/Play";


    export default {
        name: "Game",
        components: {Play}
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
    .gameSection {
        background: #F6F8F9;
        height: 1000px;
        left: 0;
        right: 0;
        margin-top: 60px;
    }

    .title {
        margin-left: 40%;
        width: 40%;
        vertical-align: middle;
        padding-top: 50px;
    }

    .buttonbox {
        border-style: solid;
        background: #ffff;
        margin-left: -11%;
    }

    .buttonboxSelect {

        border-style: solid;
        background: #D8D8D8;
    }

    .box {

        border: 5px black;
    }

    .gameArea {
        margin-top: 15%;
        padding-left: 5%;

    }

    .gameArea2 {
        margin-top: 15%;

    }


</style>