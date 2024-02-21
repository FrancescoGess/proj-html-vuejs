<script>
export default {
    name: "Latestnews",
    data(){
        return{

        }
    }
}
</script>

<template>
    <div class="container-pelicula py-5">
        <h6 class="text-uppercase fw-bold py-3">
            latest news
        </h6>

        <h2 class="text-uppercase fw-bold">
           articles update daily
        </h2>

       <div class="container-card gap-3">
            <div class="item-card">
                <img src="../assets/blog07.jpg" alt="">
                <span class="py-3">
                    November 06, 2021 By Admin
                </span>
                <h5 class="text-uppercase fw-bold">
                    recap your latest company event
                </h5>
                <span class="py-4 fw-bold ">
                    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vel nesciunt dolorem voluptatibus illum nemo quidem. Omnis mollitia, at, itaque dolor quis voluptatibus atque iure iste eligendi facilis doloribus eos sit.
                </span>
            </div>
            <div class="item-card">
                <img src="../assets/blog01.jpg" alt="">
                <span class="py-3">
                    May 27, 2022 by Admin
                </span>
                <h5 class="text-uppercase fw-bold">
                    how to edit a film score to serve
                </h5>
                <span class="py-4 fw-bold ">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique necessitatibus assumenda quos hic officiis, non blanditiis numquam! Officiis saepe cupiditate commodi, laborum eius aspernatur, accusantium ducimus aperiam, officia quasi ea?
                </span>
            </div>
            <div class="item-card">
                <img src="../assets/blog02.jpg" alt="">
                <span class="py-3">
                    November 06, 2021 By Admin
                </span>
                <h5 class="text-uppercase fw-bold">
                    recap your latest company event
                </h5>
                <span class="py-4 fw-bold ">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Est repudiandae totam, officiis sed at eligendi enim modi, aliquid quidem voluptatibus ab voluptatem sapiente ut adipisci labore neque quibusdam eum molestias.
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
            width: 400px;
        }

        span{
            color: #666666;
        }
    }
}
</style>