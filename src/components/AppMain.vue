<script>
import AboutUs from './AboutUs.vue';
import PeliculaStudio from './PeliculaStudio.vue';
import Slider from './Slider.vue';

export default{
    name:"AppMain",
    components: {
    Slider,
    PeliculaStudio,
    AboutUs
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
    </div>

 <PeliculaStudio></PeliculaStudio>
 <AboutUs></AboutUs>
</template>

<style lang="scss" scoped>

</style>