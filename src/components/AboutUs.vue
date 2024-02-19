<script>
export default {
    name: "AboutUs",
    data() {
        return {
            
        }
    },
}
</script>

<template>
    <div class="about-us">

        <div class="container-about">
            <div  class="absolute-text">
            <h6 class="text-uppercase">
                about us
            </h6>
            <h1 class="text-uppercase">
                high quality cinematics
            </h1>

            <p style="line-height: 35px;">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptate omnis voluptates assumenda, veniam explicabo ipsam odio esse id, <br>velit placeat magni molestias? Similique autem animi sint, tenetur voluptas debitis delectus.
                Lorem ipsum dolor sit amet consectetur adipisicing elit. <br>Harum atque vel incidunt, porro non ipsum dolores quo quas expedita soluta magni nam commodi, aliquid quam fuga praesentium dicta, quos iure.
            </p>

                <button style="border: none; margin-top: 30px;" class="text-uppercase fw-bold btn-light py-2 px-4">
                    read more
                </button>
        </div>
        </div>
    </div>
</template>

<style>
.about-us{
    background-image: url(../assets/About-Us.jpg);
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    height: 500px;
    color: white;

    .container-about{
        position: relative;

        .absolute-text{
            position: absolute;

            right: 100px;
            top: 100px;
        }
    }
}
</style>