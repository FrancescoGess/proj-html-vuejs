<script>
export default {
    name:"WatchList",
    data() {
        return {
            
        }
    },
}
</script>

<template>
    <div class="container-pelicula py-5">
        <h6 class="text-uppercase fw-bold py-3">
            your whatchlist
        </h6>

        <h2 class="text-uppercase fw-bold">
            best hits movies
        </h2>

       <div class="container-card">
            <div class="item-card">
                <img src="../assets/Gallery-01.jpg" alt="">
                <h5 class="text-uppercase fw-bold">
                    seventeenth summer
                </h5>
                <span class="py-4">
                    Commercial Music Video
                </span>
            </div>
            <div class="item-card my-5">
                <img src="../assets/Gallery-02.jpg" alt="">
                <h5 class="text-uppercase fw-bold">
                    a message to space
                </h5>
                <span class="py-4">
                    Short Film
                </span>
            </div>
            <div class="item-card">
                <img src="../assets/Gallery-03.jpg" alt="">
                <h5 class="text-uppercase fw-bold">
                    the most beautiful thing
                </h5>
                <span class="py-4">
                    music video
                </span>
            </div>   
       </div>

       <div class="container-card">
        <div class="item-card">
            <img src="../assets/Gallery-04.jpg" alt="">
            <h5 class="text-uppercase fw-bold">
                    permission to speak
                </h5>
                <span class="py-4">
                    Documentary
                </span>
        </div>
        <div class="item-card my-5">
            <img src="../assets/Gallery-05.jpg" alt="">
            <h5 class="text-uppercase fw-bold">
                    explore our space
                </h5>
                <span class="py-4">
                    Film noir
                </span>
        </div>
        <div class="item-card">
            <img src="../assets/Gallery-06.jpg" alt="">
            <h5 class="text-uppercase fw-bold">
                    film production
                </h5>
                <span class="py-4">
                    Blaxploitation
                </span>
        </div>   
    </div>
    </div>
</template>

<style lang="scss" scoped>
.container-pelicula{
    text-align: center;
    
   margin: 0 auto;
}

.container-card{
    padding-top: 50px;
    display: flex;
    flex-direction: row;
    gap: 50px;
    margin: 0 auto;
    height: 100%;
    width: 85%;
    .item-card{
        margin: auto;
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