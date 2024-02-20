<script>
export default{
    name: "ThirdParallax",
    data(){
        return{

        }
    }
}
</script>

<template>
    <div class="parallax">
        <div class="flex-item d-flex">
            <div class="item">
                <img src="../assets/03.png" alt="">
            </div>
            <div class="item">
                <img src="../assets/04.png" alt="">
            </div>
            <div class="item">
                <img src="../assets/05.png" alt="">
            </div>
            <div class="item">
                <img src="../assets/01.png" alt="">
            </div>
            <div class="item">
                <img src="../assets/02.png" alt="">
            </div>
            
        </div>
    </div>

</template>

<style lang="scss" scoped>
    .parallax{
        background-image: url(../assets/Parallax-01.jpg);
        background-position: bottom;
        background-repeat: no-repeat;
        background-size: cover;

        border: 2px solid white;

        height: 400px;

        .flex-item{
            width: 70%;
            margin: 0 auto;
        }
            .item{
                width: 100%;
                height: 250px;
                margin-top: 80px;

                text-align: center;
                padding-top: 80px;
            }
    }
</style>