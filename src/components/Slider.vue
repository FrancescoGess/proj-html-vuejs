<template>
    <div class="slider">
        <img 
        :src="slides[0].image " alt="pic">
        <div class="cinematic-main">
            <div class="position-object">
                <span class="text-white text-uppercase fw-bold">
                    cinemato studio
                </span>
                <h1 class="text-uppercase text-white fw-bold py-3 ">
                    action and <br>
                    inspire people
                </h1>
                <button style="border: none;" class="text-uppercase fw-bold btn-light py-2 px-4">
                    read more
                </button>

                <div class="container-left-arrow">
                    <span>
                        <a @click="prevImg" href=""><img style="width: 10px;" src="../assets/left-arrow.svg" alt=""></a>
                    </span>
                </div>

                <div class="container-right-arrow">
                    <span>
                        <a @click="nextImg" href=""><img style="width: 10px;"  src="../assets/right-arrow.svg" alt=""></a>
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default{
    name: "Slider",
    data() {
        return {
            currentImg: 0,
            autoScroll: null,
            slides: [
                {
                    image:'src/assets/cinematic.jpg'
                },
                {
                    image:'src/assets/slider2.webp'
                },
                {
                    image:'src/assets/slider3.avif'
                }
            ]
        }
    },
    methods:{
        prevImg(){
            if (this.currentImg <= 0){
                this.currentImg = this.slides.length - 1
            } else {
                this.currentImg--
            }
        }, nextImg(){
            if (this.currentImg >= this.slides.length - 1)
            this.currentImg = 0
        else{
            this.currentImg++
        }
        }, 
        currentImg(index){
            this.currentImg = index
        }
    }
}

</script>

<style lang="scss" scoped>
.cinematic-main{
    position: relative;

    .position-object{
        position: absolute;
        top: -800px;
        left: 200px;
    }

    .container-left-arrow{
        position: relative;

        span{
            position: absolute;
            top: 50px;
            left: -150px;
        }
    }
    

    .container-right-arrow{
        position: relative;

        span{
            position: absolute;
            top: 50px;
            right: -1300px;
        }
    }
    
}

.slider{
    border: 5px solid white;

    img{
        width: 100%;
    }
}
</style>