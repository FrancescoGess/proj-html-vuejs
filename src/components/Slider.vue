<template>
    <div class="slider">
        <img
        :src="slides[0].image" alt="pic">
        <div class="container-left-arrow">
        <span>
            <a @click="prevImg()" href=""><img style="width: 10px; opacity: 0.8;"  src="../assets/left-arrow.svg" alt=""></a>
        </span>
        </div>
        
        <div class="container-right-arrow">
        <span>
            <a @click="nextImg()" href=""><img style="width: 10px; opacity: 0.8;"  src="../assets/right-arrow.svg" alt=""></a>
        </span>
        </div>
        <div class="title-cinematic py-2"> 
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


        </div>

        <!-- creare funzione al click prev e next -->

     </div>
    
</template>

<script>

export default{
    name: "slider",
    data() {
        return {
            currentImg: 0,
            autoScroll: null,
            slides: [
                {
                    image:'/src/assets/cinematic.jpg'
                },
                {
                    image:'/src/assets/Cinematography-Manual.jpg'
                },
                {
                    image:'../assets/slider3.avif'
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
        }
    //     currentImg(index){
    //         this.currentImg = index
    //     }
    // },
    // created(){
    //     this.autoScroll()
    // },
    // autoScroll(){
    //         this.autoScroll = setInterval(() => {
    //             this.nextImg();
    //     }, 3000)
}}

</script>

<style lang="scss" scoped>
img{
    width: 100%;
}

.cinematic-main{
    border: 3px solid white;
    height: 200px;

    img{
        width: 100%;
    }

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
        bottom: 250px;
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
        bottom: 250px;
        right: 10px;
    }
   }
   
}

</style>