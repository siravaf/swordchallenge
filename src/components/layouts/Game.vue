<template>
    <div class="gameSection">
        <!-- Header !-->
        <div class="title">
            <h3><b>Tic Tac Toe Games</b><br></h3><br>
            <p>Welcome to the best game in the world.</p>
        </div>

        <br>
        <!-- Buttons !-->

        <div class="row">
            <div class="col-md-4" style="margin-left: 50px"></div>
            <div class="btn-group col-md-3" role="group">
                <button type="button" class="btn buttonboxSelect">Tic Tac Toe</button>
                <button type="button" class="btn buttonbox">4-in-a-row</button>
            </div>
            <div class="col-md-3"></div>
        </div>
        <br>
        <br>

        <!-- Game !-->
        <div class="row ">
            <div class="col-md-3 gameArea">
                <h1><b>Player 1</b></h1>
                <h2 style="margin-left: 30%">2</h2>
            </div>

            <div class="col-md-6">
                <div class="box">
                    <div class="app">
                        <grid></grid>
                        <button class="restart" @click="restart">Restart</button>
                    </div>
                </div>
            </div>
            <div class="col-md-3 gameArea2">
                <h1><b>Player 2</b></h1>
                <h2 style="margin-left: 20%">4</h2>
            </div>
        </div>
        <br>
        <div id="display">
            00:00:00
        </div>

    </div>


</template>

<script>

    import Grid from '@/components/layouts/Grid.vue'


    export default {
        components: {Grid},
        name: 'Game',
        data() {
            return {
                matches: 0,
                wins: {
                    O: 0,
                    X: 0,
                },
            }
        },

        methods: {
            restart() {

                Event.$emit('clearCell')

                Event.$emit('gridReset')

                this.matches++
            }

        },

        created() {
            Event.$on('win', winner => this.wins[winner]++)
            Event.$emit('clickWin', this.wins);
            Event.$emit('win', this.activePlayer)
        }
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
        height: 800px;
        left: 0;
        right: 0;
        margin-top: 80px;
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
        background: #7f8c8d;
    }

    .box {

        border: 5px black;
    }

    .gameArea {
        margin-top: 15%;
        padding-left: 10%;

    }

    .gameArea2 {
        margin-top: 15%;

    }

    .app {
        margin: 0 auto;
        width: 500px;
        color: #34495e;
    }

    .restart {
        background-color: #e74c3c;
        color: #fff;
        border: 0px;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        font-family: 'Dosis', Helvetica, sans-serif;
        font-size: 1.4em;
        font-weight: bold;
        margin: 0px;
        padding: 15px;
        width: 100%;
    }

    .restart:hover {
        background-color: #c0392b;
        cursor: pointer;
    }

    #display {
        width: 100%;
        font-size: 50px;
        margin-left: 43%;

    }

</style>