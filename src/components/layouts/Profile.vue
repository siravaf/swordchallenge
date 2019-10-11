<template>
    <div class="row">
                                <!-- Image !-->
    <div class="col-md-4">
        <img class="profileImg" alt="logo" src="@/assets/images/picture.jpg" height="120" width="120">
    </div>
    <div class="col-md-4 profile">
                                <!-- Player Info !-->
        <b><h2>Petter Griffin</h2></b>
       <p> Age: 30<br>
        Location: Porto<br>
           Occupation: Ui/Ux designer<br></p>
    </div>
                                <!-- About !-->
    <div class="col-md-4 profile">
       <p> Peter Griffin is the main character of the American animated sitcom Family Guy. ...
        Peter is married to Lois Griffin and is the father of Meg, Chris, and Stewie.
        He also has a dog named Brian, with whom he is best friends. He has worked at a toy factory,
           and at Quahog's Brewery.</p>
    </div>
    </div>
</template>

<script>
    export default {
        name:"Profile"
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

    .profileImg{
        border-radius: 50%;
        margin-left:50%;
        margin-top: 15%;
    }
    .profile{
        margin-top: 6%;
        margin-left: -3%;;
    }

    .profile3{
        margin-left:50%;
        width:40%;
        height:50%;
        text-align: right;
        vertical-align:middle;
        position: relative;
        transform: translateY(-150%);
    }
    .c{
        height:50px;
        left:0;
        right:0;
        margin-top:150px;
    }
</style>