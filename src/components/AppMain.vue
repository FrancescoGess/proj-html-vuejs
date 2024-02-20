<script>
import AboutUs from './AboutUs.vue';
import FirstParallax from './FirstParallax.vue';
import MeetTeam from './MeetTeam.vue';
import PeliculaStudio from './PeliculaStudio.vue';
import SecondParallax from './SecondParallax.vue';
import Slider from './Slider.vue';
import WatchList from './WatchList.vue';
import LatestNews from './LatestNews.vue';
import AppForm from './AppForm.vue';
import ThirdParallax from './ThirdParallax.vue';

export default{
    name:"AppMain",
    components: {
    Slider,
    PeliculaStudio,
    AboutUs,
    WatchList,
    FirstParallax,
    MeetTeam,
    SecondParallax,
    LatestNews,
    AppForm,
    ThirdParallax
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
 <SecondParallax>
</SecondParallax>
<LatestNews></LatestNews>
<ThirdParallax></ThirdParallax>
<AppForm></AppForm>
</template>

<style lang="scss" scoped>

</style>