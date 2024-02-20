<script>
export default{
    name: "TextSlider",
    data(){
        return{

        }
    }
}
</script>


<template>
    <div class="text-slider">
        <div class="absolute-container">
        <h1>
            &#10077;
        </h1>

        <p>
            Un designer ha il dovere di creare un design senza tempo. Per essere senza tempo devi pensare molto <br>lontano nel futuro, non il prossimo anno, non tra due anni, <br> ma tra un minimo di 20 anni. 
        </p>

    <div class="d-flex container-pic-citazione gap-3 align-items-center">
        <figure>
            <img src="../assets/03.jpg" alt="person">
        </figure>
        <div class="d-flex row">
        <span class="text-uppercase fw-bold">
            Phillip Starck
        </span>
        <span>
            Designer
        </span>
        </div>
    </div>
        <!-- - Phillip Starck, creatore, designer e architetto -->
    </div>
    </div>
</template>

<style lang="scss" scoped>
    .text-slider{
        width: 100%;
        height: 800px;

        position: relative;
        color: white;

        .absolute-container{
            position: absolute;
            top: -550px;
            left: 700px;
        }

        .container-pic-citazione figure img{
            border-radius: 50px;
        }
    }
</style>