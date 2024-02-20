<script>
export default{
    name: "FirstParallax",
    data(){

    }
}
</script>

<template>
    <div class="parallax">
        <div class="flex-item d-flex">
            <div class="item">
                <h1 class="fw-bold text-white">
                    158
                </h1>
                <span class="text-uppercase text-white fw-bold ">
                    satisfied clients
                </span>
            </div>
            <div class="item">
                <h1 class="fw-bold text-white">
                    3+
                </h1>
                <span class="text-uppercase text-white fw-bold ">
                    our projects
                </span>
            </div>
            <div class="item">
                <h1 class="fw-bold text-white">
                    1,906
                </h1>
                <span class="text-uppercase text-white fw-bold ">
                    cup of coffee
                </span>
            </div>
            <div class="item">
                <h1 class="fw-bold text-white">
                    2
                </h1>
                <span class="text-uppercase text-white fw-bold ">
                    our awards
                </span>
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