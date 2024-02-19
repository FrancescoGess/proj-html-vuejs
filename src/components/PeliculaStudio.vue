<script>
export default{
    name: "PeliculaStudio",
    data(){
        return
    }
}
</script>

<template>
    <div class="container-pelicula py-5">
        <h6 class="text-uppercase fw-bold py-3">
            PeliculaStudio
        </h6>

        <h2 class="text-uppercase fw-bold">
            this is what we do
        </h2>

       <div class="container-card">
            <div class="item-card">
                <img src="../assets/image (14).svg" alt="">
                <span class="py-4">
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Lorem ipsum dolor sit amet consectetur.
                </span>
            </div>
            <div class="item-card my-5">
                <img src="../assets/image (16).svg" alt="">
                <span class="py-4">
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Lorem ipsum dolor sit amet consectetur.
                </span>
            </div>
            <div class="item-card">
                <img src="../assets/image (18).svg" alt="">
                <span class="py-4">
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Lorem ipsum dolor sit amet consectetur.
                </span>
            </div>   
       </div>

       <div class="container-card">
        <div class="item-card">
            <img src="../assets/image (15).svg" alt="">
            <span class="py-4">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Lorem ipsum dolor sit amet consectetur.
            </span>
        </div>
        <div class="item-card my-5">
            <img src="../assets/image (17).svg" alt="">
            <span class="py-4">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Lorem ipsum dolor sit amet consectetur.
            </span>
        </div>
        <div class="item-card">
            <img src="../assets/image (19).svg" alt="">
            <span class="py-4">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Lorem ipsum dolor sit amet consectetur.
            </span>
        </div>   
   </div>

        <!-- <div class="container text-center">
            <div class="row">
              <div class="col">
                
              </div>
              <div class="col">
                
              </div>
              <div class="col">
                
              </div>
            </div>
          </div> -->
    </div>
</template>

<style lang="scss" scoped>
.container-pelicula{
    text-align: center;
    
   margin: 0 auto;
}

.container-card{
    padding-top: 50px;
    display: flex;
    flex-direction: row;
    gap: 50px;
    margin: 0 auto;
    height: 100%;
    width: 85%;

    .item-card{
        margin: auto;
        width: calc(100%/3);
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;

        img{
            width: 200px;
        }

        span{
            color: grey;
        }
    }
}
</style>