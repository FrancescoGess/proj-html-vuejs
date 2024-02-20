<script>
export default{
    name: "AppForm",
    data(){
        return{

        }
    }
}
</script>

<template>
    <div class="container-flex d-flex">
        <div class="container-description col-6 p-5">
            <div class="container-work mx-5 ">
                <h5 class="text-uppercase fw-bold">
                    collaborate
                </h5>
                <h1 class="text-uppercase fw-bold">
                    want to work with us?<br>
                    leave us a message!
                </h1>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam in natus id eos maxime amet nemo dolores voluptatem asperiores libero, dignissimos consectetur praesentium, quas sapiente a dicta. Sit, eum alias? Lorem ipsum, dolor sit amet consectetur adipisicing elit. In, provident est? Ad repudiandae natus dicta, facilis, nisi error facere culpa obcaecati iusto, a ipsa. Error ex fugit voluptas blanditiis incidunt.
                </p>
            </div>
        </div>
        <div class="col-6 p-5">
            <div class="container-form mx-5">
                <form>
                    <div class="form-row">
                      <div class="form-group col-md-6 d-flex gap-5">
                        <input style="background-color: #66666619;" type="text" class="p-2 px-4  rounded-0 border-0 " placeholder="Your Name">
                        <input style="background-color: #66666619;" type="email" class="p-2 px-4 rounded-0 border-0" placeholder="Your email">
                      </div>
                      <div class="form-group col-md-6 d-flex gap-5 py-4 ">
                        <input style="background-color: #66666619;" type="number" class="p-2 px-4 rounded-0 border-0" placeholder="Mobile number">
                        <input style="background-color: #66666619;" type="password" class="p-2 px-4 rounded-0 border-0" id="inputPassword4" placeholder="Your Pincode">
                      </div>
                    </div>
                    
                    <textarea style="background-color: #66666619; border: none;" name="text" id="" cols="65" rows="10" class="p-3" placeholder="Enter your message"></textarea>
                    <div class="btn-custom">
                        <button type="submit" class="rounded-0 fw-bold btn btn-dark p-2 px-5">SUBMIT NOW</button>
                    </div>
                  </form>
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
.container-flex{
    height: 800px;

    .container-form{
        padding: 100px;
    }

    .container-work{
        padding: 100px;

        p{
            color: #666666;
            line-height: 35px;
            padding-top: 20px;
        }
    }
}
</style>