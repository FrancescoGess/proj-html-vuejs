<script>
import AboutUs from './AboutUs.vue';
import PeliculaStudio from './PeliculaStudio.vue';
import Slider from './Slider.vue';
import WatchList from './WatchList.vue';

export default{
    name:"AppMain",
    components: {
    Slider,
    PeliculaStudio,
    AboutUs,
    WatchList
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
</template>

<style lang="scss" scoped>

</style>