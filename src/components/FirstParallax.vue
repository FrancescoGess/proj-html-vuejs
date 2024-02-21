<script>
export default{
    name: "FirstParallax",
    data(){
        return{
            contatoreCoffee: 0,
            contatoreClients: 0,
            contatoreAwards: 0,
            timer: null
        }
    },
    mounted(){
        this.timer = setInterval(() => {
            if (this.contatoreCoffee < 1906){
                this.contatoreCoffee ++
            }else {
                clearInterval(this.timer) // per fermare il conteggio 
                setTimeout(()=> {
                    this.contatoreCoffee = 0 // riavvia il conteggio dopo tot secondi(2 in questo caso)
                    this.timer = setInterval(()=>{
                        if (this.contatoreCoffee < 1906 ) {
                            this.contatoreCoffee ++
                        } else{
                            clearInterval(this.timer)
                        }
                    },0.5)
                }, 2000)
            }
        }, 0.5)
    },
    beforeUnmount() {
    clearInterval(this.timer) // Assicuriamoci di pulire l'intervallo quando l'istanza Vue viene distrutta
    }}

</script>

<template>
    <div class="parallax">
        <div class="flex-item d-flex">
            <div class="item">
                <h1 class="fw-bold text-white">
                    158
                </h1>
                <span class="text-uppercase text-white fw-bold ">
                    satisfied clients
                </span>
            </div>
            <div class="item">
                <h1 class="fw-bold text-white">
                    3+
                </h1>
                <span class="text-uppercase text-white fw-bold ">
                    our projects
                </span>
            </div>
            <div class="item">
                <h1 class="fw-bold text-white">
                    {{ contatoreCoffee }}
                </h1>
                <span class="text-uppercase text-white fw-bold ">
                    cup of coffee
                </span>
            </div>
            <div class="item">
                <h1 class="fw-bold text-white">
                    2
                </h1>
                <span class="text-uppercase text-white fw-bold ">
                    our awards
                </span>
            </div>
            
        </div>
    </div>

</template>

<style lang="scss" scoped>
    .parallax{
        background-image: url(../assets/Parallax-01.jpg);
        background-position: bottom;
        background-repeat: no-repeat;
        background-size: cover;

        border: 2px solid white;

        height: 400px;

        .flex-item{
            width: 70%;
            margin: 0 auto;
        }
            .item{
                width: 100%;
                height: 250px;
                margin-top: 80px;

                text-align: center;
                padding-top: 80px;
            }
    }
</style>