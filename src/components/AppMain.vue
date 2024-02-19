<script>
import PeliculaStudio from './PeliculaStudio.vue';
import Slider from './Slider.vue';

export default{
    name:"AppMain",
    components: {
    Slider,
    PeliculaStudio
},
    data() {
        return {
            
        }
    }
    }
</script>

<template>
    <!-- creare slider -->
    <div class="cinematic-main">
        <Slider></Slider>
        <!-- <img src="../assets/cinematic.jpg" alt="slider"> -->
    </div>

    <!-- <PeliculaStudio></PeliculaStudio> -->
</template>

<style lang="scss" scoped>

</style>