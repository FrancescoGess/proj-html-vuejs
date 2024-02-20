<script>
import AboutUs from './AboutUs.vue';
import FirstParallax from './FirstParallax.vue';
import MeetTeam from './MeetTeam.vue';
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
    FirstParallax,
    MeetTeam
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
 <MeetTeam></MeetTeam>
</template>

<style lang="scss" scoped>

</style>