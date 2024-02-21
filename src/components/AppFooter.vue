<script>

export default{
    name: "AppFooter",
    data() {
    return {
      footerColumns: [
        {
          title: "contact info",
          items: [
            {
              icon: "src/assets/footer-location-dot-solid.svg",
              text: "2/45 Tower Street, New York USA"
            },
            {
              icon: "src/assets/footer-phone-solid.svg",
              text: "Call Us On 0800 840 1010"
            },
            {
              icon: "src/assets/footer-envelope-soli.svg",
              text: "Demo@Example.com"
            }
          ]
        },
        {
          title: "get help",
          list: [
            { link: "#", text: "FAQ" },
            { link: "#", text: "shipping" },
            { link: "#", text: "returns" },
            { link: "#", text: "order status" },
            { link: "#", text: "payment options" }
          ]
        },
        {
          title: "online shop",
          list: [
            { link: "#", text: "watch" },
            { link: "#", text: "bag" },
            { link: "#", text: "shoes" },
            { link: "#", text: "dress" }
          ]
        },
        {
          title: "newsletter",
          form: {
            text: "Subscribe To Receive Inspiration, Ideas & News In Your Inbox",
            placeholder: "Enter Your email",
            buttonText: "subscribe"
          }
        }
      ]
    };
  }
}
</script>

<template>
<footer>

  <div class="container">
    <div class="row">
      <div v-for="(column, index) in footerColumns" :key="index" class="footer-col">
        <h4 v-if="column.title" :class="{'text-uppercase': column.uppercase}">{{ column.title }}</h4>
        <div v-if="column.items" v-for="(item, itemIndex) in column.items" :key="itemIndex" class="d-flex container-foot gap-3">
          <img v-if="item.icon" :src="item.icon" alt="" />
          <span>{{ item.text }}</span>
        </div>
        <ul v-if="column.list" v-for="(listItem, listItemIndex) in column.list" :key="listItemIndex">
          <li><a :href="listItem.link">{{ listItem.text }}</a></li>
        </ul>
        <div v-if="column.form" class="form-mail">
          <span>{{ column.form.text }}</span>
          <form class="py-4">
            <input style="background-color: #66666619;" type="email" class="p-2 px-4 rounded-0 border-0" :placeholder="column.form.placeholder">
          </form>
          <button style="border: none; background-color: white;" class="text-uppercase fw-bold btn-light py-2 px-4">
            {{ column.form.buttonText }}
          </button>
        </div>
      </div>
  
    <!-- <div class="container">
      <div class="row">
        <div class="footer-col">
          <h4 class="text-uppercase">contact info</h4>
          <div class="d-flex container-foot gap-3">
              <img src="../assets/footer-location-dot-solid.svg" alt="">
            <span>
              2/45 Tower Street, New York USA
            </span>
          </div>
          <div class="d-flex container-foot gap-3">
              <img src="../assets/footer-phone-solid.svg" alt="">
            <span>
              Call Us On 0800 840 1010
            </span>
          </div>
          <div class="d-flex container-foot gap-3">
              <img src="../assets/footer-envelope-soli.svg" alt="">
            <span>
              Demo@Example.com
            </span>
          </div>
        </div>
        <div class="footer-col">
          <h4>get help</h4>
          <ul>
            <li><a href="#">FAQ</a></li>
            <li><a href="#">shipping</a></li>
            <li><a href="#">returns</a></li>
            <li><a href="#">order status</a></li>
            <li><a href="#">payment options</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h4>online shop</h4>
          <ul>
            <li><a href="#">watch</a></li>
            <li><a href="#">bag</a></li>
            <li><a href="#">shoes</a></li>
            <li><a href="#">dress</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h4 class="text-uppercase">newsletter</h4>
          <div class="form-mail">
            <span>
              Subscribe To Receive Inspiration, <br>
              Ideas & News In Your Inbox
            </span>
            <form class="py-4">
              <input style="background-color: #66666619;" type="email" class="p-2 px-4 rounded-0 border-0" placeholder="Enter Your email">
            </form>
            <button style="border: none; background-color: white;" class="text-uppercase fw-bold btn-light py-2 px-4">
            subscribe
        </button>
          </div>
        </div> -->

        <div class="py-1">
        </div>
        <hr style="color: white;">
      </div>

      <div class="container-copyright">
        <span>
          &#9426; 2023 All Rights Reserved. Developed By Frank Gess
        </span>
      </div>
     </div>
    </footer>
</template>

<style lang="scss" scoped>


*{
    background-color: #111111;
    line-height: 1.5;
    margin:0;
    padding:0;
    box-sizing: border-box;
  }
  .container-copyright{
    margin: 0 auto;
    text-align: center;

    span{
      color: white;
    }
  }

.container-foot{
  color: #bbbbbb;
  font-weight: bold;
  padding-top: 15px;
}

img{
  width: 20px;
  text-align: center;
  align-items: center;
}

.form-mail{
  color: #bbbbbb;
}
.container{ 
  margin:auto;

}
.row{
  padding: 30px;
  display: flex;
  flex-wrap: wrap;
}
ul{
  list-style: none;
}
.footer{
    height: 300px;
    padding: 70px 0;
}
.footer-col{
   width: 25%;
   padding: 0 15px;
}
.footer-col h4{
  font-size: 18px;
  color: #ffffff;
  text-transform: capitalize;
  margin-bottom: 35px;
  font-weight: 500;
  position: relative;
}

.footer-col ul li:not(:last-child){
  margin-bottom: 10px;
}
.footer-col ul li a{
  font-size: 16px;
  text-transform: capitalize;
  color: #ffffff;
  text-decoration: none;
  font-weight: 300;
  color: #bbbbbb;
  display: block;
  transition: all 0.3s ease;
}
.footer-col ul li a:hover{
  color: #ffffff;
  padding-left: 8px;
}
.footer-col .social-links a{
  display: inline-block;
  height: 40px;
  width: 40px;
  background-color: rgba(255,255,255,0.2);
  margin:0 10px 10px 0;
  text-align: center;
  line-height: 40px;
  border-radius: 50%;
  color: #ffffff;
  transition: all 0.5s ease;
}
.footer-col .social-links a:hover{
  color: #ffffff;
  background-color: #111111;
}

</style>