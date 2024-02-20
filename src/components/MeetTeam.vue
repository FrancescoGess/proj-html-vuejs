<script>
export default{
    name: "MeetTeam",
        data() {
        return {
            
        }
    },
}
</script>

<template>
     <div class="container-pelicula py-5">
        <h6 class="text-uppercase fw-bold py-3">
            the pericuros
        </h6>

        <h2 class="text-uppercase fw-bold">
            meet the team
        </h2>

       <div class="container-card">
            <div class="item-card">
                <img src="../assets/Team-01.jpg" alt="">
                <h5 class="text-uppercase fw-bold">
                    fabricio guerra
                </h5>
                <span class="py-4">
                    Main Director
                </span>
            </div>
            <div class="item-card">
                <img src="../assets/Team-02.jpg" alt="">
                <h5 class="text-uppercase fw-bold">
                    umberto pagoda
                </h5>
                <span class="py-4">
                    Main Writer
                </span>
            </div>
            <div class="item-card">
                <img src="../assets//Team-03.jpg" alt="">
                <h5 class="text-uppercase fw-bold">
                    gloria riccasso
                </h5>
                <span class="py-4">
                    Main Producer
                </span>
            </div>   

            <div class="item-card">
            <img src="../assets/Team-04.jpg" alt="">
            <h5 class="text-uppercase fw-bold">
                    lio napoin
                </h5>
                <span class="py-4">
                    Cameraman
                </span>
            </div>
       </div>
    </div>

</template>

<style lang="scss" scoped>
.container-pelicula{
    text-align: center;
    width: 80%;
    margin: 0 auto;
}

.container-card{
    padding-top: 50px;
    display: flex;
    flex-direction: row;

    .item-card{
        margin: 0 auto;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;

        h5{
            padding-top: 20px;
        }

        img{
            width: 100%;
        }

        span{
            color: #666666;
        }
    }
}
</style>