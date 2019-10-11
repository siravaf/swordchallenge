<template>
    <!-- Header !-->
    <div class="container">
        <div class="title">
            <h1><b>Awesome Statistics</b></h1><br>
            <div class="subTitle">
                <p>All statistics in one place!</p>
            </div>
        </div>
        <br>

        <div class="row" style="margin-left: 20%">
            <div class="col-md-6">
                <h3><b>Game victories%</b></h3>
                <div class="row">
                    <div class="col-md-5"><p>Player 1</p></div>
                    <div class="col-md-5"><p>Player 2</p></div>
                </div>

                <div class="row">
                    <div class="col-md-4">
                        <div class="circle"></div>
                        <div class="circle"></div>
                    </div>
                    <div class="col-md-4">
                        <div class="circle"></div>
                        <div class="circle"></div>
                    </div>
                </div>


            </div>
            <div class="col-md-6">
                <h3><b>Played matches</b></h3>
                <br>

                <div class="row">
                    <div class="col"><img width="25%" hspace="5" alt="logo" src="@/assets/images/X_bright.svg"></div>
                    <div class="col"><img width="25%" hspace="5" alt="logo" src="@/assets/images/X_bright.svg"></div>
                    <div class="col"><img width="25%" hspace="5" alt="logo" src="@/assets/images/X_bright.svg"></div>
                    <div class="col"></div>
                </div>
            </div>


        </div>
        <br>
        <div id="display">
            <h3 style="margin-left: 3%"><b>Total time</b></h3>
            00:42:13
        </div>

    </div>


</template>

<script>
    export default {
        name: "Stats"
    }

</script>


<style scoped>
    @font-face {
        src: url('/src/assets/fonts/glacialindifference-regular-webfont.ttf');
        font-family: glacial;
    }

    @font-face {
        src: url('/src/assets/fonts/glacialindifference-bold-webfont.ttf');
        font-family: bglacial;
    }

    p {
        font-family: glacial;
    }

    b {
        font-family: bglacial;
    }

    .container {
        margin-top: 70px;
    }

    .title {
        margin-left: 35%;
        width: 40%;
        vertical-align: middle;
        margin-top: 5px;
    }

    .subTitle {
        margin-left: 15%
    }

    #display {
        width: 100%;
        font-size: 50px;
        margin-left: 40%;

    }

    .circle {
        border-radius: 50%;
        display: inline-block;
        height: 50px;
        width: 50px;
        background-color: #838383;
    }

    .col {
        padding-left: 0px;
    }
</style>

