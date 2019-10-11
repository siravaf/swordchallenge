<template>

    <div class="row footer">
                                    <!-- Section 1 !-->
        <div class="col-md-2"></div>
        <div class="col-md-3 ml-3">
            <p><b>About Page</b><br><br>
                Play tic tac toe or 4 in-a-row anytime!<br>
            Created by António Ferreira</p>
        </div>

                                    <!-- Section 2 !-->
        <div class="col-md-3 ml-2">
            <p><b>Contacts</b><br><br>
                (+351)123 456 789<br>
                Rua Sá da Bandeira, 111, Porto</p>
        </div>
                                    <!-- Section 3 !-->
        <div class="col-md-3 ml-3">
            <p><b>Stay in touch</b><br><br>
                <img width="10%" hspace="5" alt="logo" src="@/assets/images/facebook.svg">
                <img width="10%" hspace="5" alt="logo" src="@/assets/images/twitter.svg">
                <img width="10%" hspace="5" alt="logo" src="@/assets/images/instagram.svg"><br>
                <input type="text" name="newsletter">
                <img width="10%" alt="logo" class="button" src="@/assets/images/send.svg"></p>
        </div>
        </div>

</template>

<script>
    export default {
        name:"Footer"
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
    .footer{
        background:#F6F8F9;
        height:170px;
        left:0;
        right:0;
        bottom: 0;
    }
    .footer1{
        margin-left:3px;
     }
    .footer2{
        margin-left:40%;
        padding-right: 10px;
        padding-left: 10px;
        width:20%;
        height:50%;
     }
    .footer3{
        margin-left: 75%;
        width:20%;
     }
    .button{
        background-color:black;
    }

</style>