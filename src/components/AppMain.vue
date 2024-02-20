<script>
import AboutUs from './AboutUs.vue';
import FirstParallax from './FirstParallax.vue';
import PeliculaStudio from './PeliculaStudio.vue';
import Slider from './Slider.vue';
import WatchList from './WatchList.vue';

export default{
    name:"AppMain",
    components: {
    Slider,
    PeliculaStudio,
    AboutUs,
    WatchList,
    FirstParallax
},
    data() {
        return {
            
        }
    }
    }
</script>

<template>

 <Slider></Slider> 
 <PeliculaStudio></PeliculaStudio>
 <AboutUs></AboutUs>
 <WatchList></WatchList>
 <FirstParallax></FirstParallax>
</template>

<style lang="scss" scoped>

</style>