<script>
export default{
    name:"AppMain"
}
</script>

<template>

    <!-- creare slider -->
    <div class="cinematic-main">
        <div class="title-cinematic py-2">
            <span class="text-white text-uppercase fw-bold">
                cinemato studio
            </span>
            <h1 class="text-uppercase text-white fw-bold py-3 ">
                action and <br>
                inspire people
            </h1>

            <!-- creare funzione al click per leggere del testo -->
            <button class="text-uppercase fw-bold btn-light py-2 px-4">
                read more
            </button>

        </div>

        <!-- creare funzione al click prev e next -->
        <div class="container-left-arrow">
            <span>
                <a href=""><img style="width: 10px; opacity: 0.8;"  src="../assets/left-arrow.svg" alt=""></a>
            </span>
        </div>

        <div class="container-right-arrow">
            <span>
                <a href=""><img style="width: 10px; opacity: 0.8;"  src="../assets/right-arrow.svg" alt=""></a>
            </span>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.cinematic-main{
    border: 3px solid white;
    height: 600px;

   background-image: url(../assets/cinematic.jpg);
   background-repeat: no-repeat;
   background-size: cover;
   background-position: center;

   .title-cinematic{
    height: 300px;
    width: 75%;
    margin: 0 auto;

    margin-top: 150px;

    .btn-custom{
        margin-top: 20px;
    }

   }

   .container-left-arrow{
    position: relative;
    
    span{
        padding: 15px;
        
        background-color: black;
        opacity: 0.7;


        position: absolute;
        bottom: 100px;
        left: 10px;
    }
   }

   .container-right-arrow{
    position: relative;
    
    span{
        padding: 15px;
        
        background-color: black;
        opacity: 0.7;


        position: absolute;
        bottom: 100px;
        right: 10px;
    }
   }
   
}
</style>