<script>
export default{
    name: "SecondParallax",
    data(){
        return{
            images:[
                'src/assets/parallax-02.jpg',
                'src/assets/cinematic-street-photography-1.jpg',
                'src/assets/fstoppers_cinematic_challenge_davidgeffin_dennis1.jpg',
                'src/assets/4349192.jpg'
            ],
            timer: null,
            currentIndex: 0
        };
    },
   mounted: function(){
       this.startSlide()
   },
    methods:{
         startSlide: function(){
              this.timer = setInterval(this.next, 3000)
          },
        next: function() {
            this.currentIndex += 1;
        },
        prev: function() {
            this.currentIndex -= 1;
    }
    },
    computed: {
    currentImg: function() {
      return this.images[Math.abs(this.currentIndex) % this.images.length];
    }
  }

}
</script>

<template>
  <div class="text-slider">
        <div class="absolute-container">
        <h1>
            &#10077;
        </h1>

        <p>
            Un designer ha il dovere di creare un design senza tempo. Per essere senza tempo devi pensare molto <br>lontano nel futuro, non il prossimo anno, non tra due anni, <br> ma tra un minimo di 20 anni. 
        </p>

    <div class="d-flex container-pic-citazione gap-3 align-items-center">
        <figure>
            <img src="../assets/03.jpg" alt="person">
        </figure>
        <div class="d-flex row">
        <span class="text-uppercase fw-bold">
            Phillip Starck
        </span>
        <span>
            Designer
        </span>
        </div>
    </div>
        <!-- - Phillip Starck, creatore, designer e architetto -->
    </div>
    </div>

    <div>
    <transition-group name="fade" tag="div">
      <div v-for="i in [currentIndex]" :key="i">
        <img class="img-slide" :src="currentImg"/>
      </div>
    </transition-group>
    <a class="prev" @click="prev" href="#">&#10094; Previous</a>
    <a class="next" @click="next" href="#">&#10095; Next</a>
  </div>

</template>

<style lang="scss" scoped>
.text-slider{
        

        position: relative;
        color: white;

        .absolute-container{
            position: absolute;

            top: 300px;
            left: 35%;
            
        }

        .container-pic-citazione figure img{
            border-radius: 50px;
        }
    }

 .fade-enter-active,
 .fade-leave-active {
   overflow: hidden;
   visibility: visible;
   position: absolute;
   width:100%;
   opacity: 1;
 }

 .fade-enter,
 .fade-leave-to {
   visibility: hidden;
   width:100%;
   opacity: 0;
 }

 .img-slide {
   height:800px;
   width:100%;
 }

// .prev, .next {
//   cursor: pointer;
//   position: absolute;
//   top: 40%;
//   width: auto;
//   padding: 16px;
//   color: white;
//   font-weight: bold;
//   font-size: 18px;
//   transition: 0.7s ease;
//   border-radius: 0 4px 4px 0;
//   text-decoration: none;
// }

// .next {
//   right: 0;
// }

// .prev {
//   left: 0;
// }

// .prev:hover, .next:hover {
//   background-color: rgba(0,0,0,0.9);
// }
</style>