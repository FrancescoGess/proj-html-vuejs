<template>
    <div class="slider">
        <div class="text-slider">
            <div class="position-text p-2">

<div class="container-about text-white fw-bold">
    <div  class="absolute-text">
    <h6 class="text-uppercase">
        cinemato studio
    </h6>
    <h1 class="text-uppercase">
        {{ list[currentIndex].title }}
    </h1>


<button style="border: none; margin-top: 30px;" class="text-uppercase fw-bold btn-light py-2 px-4">
    read more
</button>
</div>
</div>
</div>
        </div>
            <div>
                <div name="fade" tag="div">
                    <div v-for="i in [currentIndex]" :key="i">
                        <img :src="list[i].image"/>
                    </div>
                    <!-- <img :src="list[currentIndex].image"/> -->
                </div>
            </div>
                <a class="prev" @click="prev" href="#">&#10094;</a>
                <a class="next" @click="next" href="#">&#10095;</a>
    </div>
</template>

<script>

export default{
    name: "Slider",
    data(){
        return{
            showModal: false,
            list: [
            {
                image: 'src/assets/cinematic.jpg',
                title: 'action and inspire people'
            },
            {
                image: 'src/assets/slider2.webp',
                title: 'cinematic slideshow'
            },
            {
                image: 'src/assets/slider3.avif',
                title: 'fireborn cinematic trailer'
            },
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
            if(this.currentIndex + 1 == this.list.length){
                this.currentIndex = 0
            } else{
                this.currentIndex = this.currentIndex + 1
            }
        },
        prev: function() {
            if( (this.currentIndex - 1) < 0 ){
            this.currentIndex = this.list.length - 1
        } else {
            this.currentIndex = this.currentIndex - 1
        }},
        openModal(){
            this.showModal = true
        },
        closeModal(){
            this.showModal = false
        }
    },


}

</script>


<style lang="scss" scoped>

.modal {
  display: none; /* Per default la finestra modale è nascosta */
  position: fixed; /* Posizionamento fisso per sovrapporsi al contenuto */
  z-index: 1; /* Ordine di sovrapposizione */
  left: 0;
  top: 0;
  width: 100%; /* Occupa l'intera larghezza */
  height: 100%; /* Occupa l'intera altezza */
  background-color: rgba(0,0,0,0.5); /* Sfondo semi-trasparente */
  overflow: auto; /* Scorrimento per contenuti che superano la finestra */
}

.modal-content {
  background-color: #fefefe; /* Colore di sfondo */
  margin: 15% auto; /* Margin per centrare verticalmente */
  padding: 20px;
  border: 1px solid #888;
  width: 80%; /* Larghezza del contenuto */
  max-width: 600px; /* Larghezza massima */
}

.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: black;
  text-decoration: none;
  cursor: pointer;
}
.text-slider{
    position: relative;

    .position-text{
        position: absolute;
        top: 500px;
        left: 30%;
    }
}

.fade-enter-active,
.fade-leave-active {
  overflow: hidden;
  visibility: visible;
  position: absolute;
  width: 100%;
  opacity: 1;
}

.fade-enter,
.fade-leave-to {
  visibility: hidden;
  width:100%;
  opacity: 0;
}

img {
  height: 1200px;
  width: 100%;
}

.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.7s ease;
  border-radius: 0 4px 4px 0;
  text-decoration: none;
}

.next {
  right: 0;
  
}

.prev {
  left: 0;
}


.slider{
    border: 5px solid white;

    img{
        width: 100%;
    }
}
</style>