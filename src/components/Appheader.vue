<script>
import IconSvg from './iconSvg.vue';
export default {
        name: "AppHeader",
        data() {
            return {
                navLinks: [
                    {
                        name: "home",
                        
                    },
                    {
                        name: "blog",
                    
                    },
                    {
                        name: "pages",
                        showDropdown: false,
                        dropdownItems: [
                            { name: "Il nostro blog", url: "#" },
                            { name: "Dai un'occhiata ai nostri fumetti", url: "#" },
                            { name: "su di noi ...", url: "#" },
                        ],
                    },
                    {
                        name: "about",
                    
                    },
                    {
                        name: "contacts",
                    
                    },
                    {
                        name: "gallery",
                    
                    },
                    {
                        name: "shop",
                        showDropdown: false,
                        dropdownItems: [
                            { name: "cinematic", url: "#" },
                            { name: "gift card", url: "#" },
                            { name: "merchandise", url: "#" },
                        ],
                    },
                ],
            };
        },
        components: {
            IconSvg
        },
        methods: {
            showDropdown(index) {
                this.navLinks[index].showDropdown = true;
            },
            hideDropdown(index) {
                this.navLinks[index].showDropdown = false;
            },
        },
    };
</script>

<template>

    <div class="head-page p-2 d-flex justify-content-between align-items-center">
            <!-- LOGO -->
            <div class="container-logo p-3">
                <figure>
                    <a href="#"><img src="../assets/logo.svg" alt="logo footer"></a>
                </figure>
            </div>

            <div>
    <nav>
        <ul class="navbar-flex d-flex gap-5 my-2">
            <li v-for="(element, index) in navLinks" :key="index">
                <a href="#" @mouseover="showDropdown(index)" @mouseleave="hideDropdown(index)">
                    {{ element.name }}
                    <ul v-if="element.showDropdown && (element.name === 'pages' || element.name === 'shop')" class="dropdown-menu rounded-0 ">
                        <li v-for="(item, i) in element.dropdownItems" :key="i">
                            <a :href="item.url">{{ item.name }}</a>
                        </li>
                    </ul>
                </a>
            </li>
        </ul>
    </nav>
</div>

            <!-- NAVBAR -->
            <!-- <div>
                <nav>
                    <ul class="navbar-flex d-flex gap-5 my-2">
                        <li 
                        v-for="(element, index) in navLinks"
                        :key="index">
                            <a href="#">{{ element.name }}</a>
                        </li>
                    </ul>
                </nav>
                
            </div> -->

            <!-- SOCIAL LINKS -->
            <div class="icons">

                <IconSvg>

                </IconSvg>


            </div>
        </div>
</template>

<style lang="scss" scoped>

.dropdown-menu {
        display: none;
        position: absolute;
        background-color: black;
        min-width: 260px;
        box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
        padding: 10px;
    }
    .dropdown-menu a {
            text-decoration: none;
            text-transform: uppercase;
            color: white;
            font-weight: bold;
            padding: 10px;
            
    
    }
    
    li:hover .dropdown-menu {
        display: block;
        background-color: black;

        li a{
            color: #ffffff;
        }
    }

 .head-page{
     background-color: #ffffff;
     /* position: fixed; */
     top: 0;
     width: 100%;
     overflow: hidden;
 }

 .container-logo { 
     width: 250px;
 }

 .navbar-flex{
    
     list-style-type: none;
         a{
             text-decoration: none;
             text-transform: uppercase;
             
             color: black;
             font-weight: bold;
            }
        
        }
</style>