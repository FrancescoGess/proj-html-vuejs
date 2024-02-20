<script>
export default{
    name: "SecondParallax",
    data(){
        return{
          list: [
            {
                image: 'src/assets/Parallax-02.jpg',
                title: 'action and inspire people',
                active: true,
                description: 'lorem ipsum'
            },
            {
                image: 'src/assets/cinefy.webp',
                title: 'test',
                active: false,
                description: 'lorem ipsum'
            },
            {
                image: 'src/assets/cinefy2.webp',
                title: 'test2',
                active: false,
                description: 'lorem ipsum'
            },
            ],
            currentIndex: 0
        };
    }
   }
    methods:{
    




    //  startSlide: function(){
    //       this.timer = setInterval(this.next, 3000)
    //   },
    //     next: function() {
    //         if (this.currentIndex + 1 == this.list.lenght){
    //         this.currentIndex = 0
    //       } else{
    //         this.currentIndex = this.currentIndex + 1
    //       }
    //     },
    //     prev: function() {
    //         if ( this.currentIndex - 1 < 0 ){
    //           this.currentIndex = this.list.lenght - 1
    //         } else{
    //           this.currentIndex = this.currentIndex - 1
    //         }
    // }
    }
</script>

<template>
  

    <div id="carouselExampleIndicators" class="carousel slide">
  <div class="carousel-indicators">
    <button @click="this.currentIndex = 0" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
    <button @click="this.currentIndex = 1" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
    <button @click="this.currentIndex = 2" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
  </div>
  <div class="carousel-inner">
    <div 
    v-for="i in list" :key="i"
    class="carousel-item"
    :class="{active: i.active}">
      <img :src="i.image" class="d-block w-100 h-50" alt="slider">
    </div>
  </div>
</div>

<div class="text-slider">
        <div class="absolute-container">
        <h1>
            &#10077;
        </h1>

        <p>
            {{list[currentIndex].description}} 
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
   <!-- <div>
    <transition-group name="fade" tag="div">
      <div v-for="i in [currentIndex]" :key="i">
        <img class="img-slide" :src="currentImg"/>
      </div>
    </transition-group>
  </div> -->

</template>

<style lang="scss" scoped>

.text-slider{
        position: relative;
        color: white;

        .absolute-container{
            position: absolute;
            bottom: 500px;
            left: 25%;

            font-size: 30px;
            
        }

        .container-pic-citazione{
          font-size: 30px;
        }

        
        .container-pic-citazione figure img{
          width: 80px;
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

 .fade-enter
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