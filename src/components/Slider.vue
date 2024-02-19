<template>
    <div class="slider">
        <img :src=" slides.image " alt="slider">
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
                    image:'../assets/cinematic.jpg'
                },
                {
                    image:'../assets/slider2.webp'
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
        }, 
        currentImg(index){
            this.currentImg = index
        }
    }
}

</script>