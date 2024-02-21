<script>
import IconSvg from './iconSvg.vue';



export default{
    name: "AppHeader",
    data() {
        return {
            dropDownVisible: false,
            navLinks: [
                {
                    name: 'home',
                },
                {
                    name: 'blog',
                },
                {
                    name: 'pages',
                },
                {
                    name: 'about',
                },
                {
                    name: 'contacts',
                },
                {
                    name: 'gallery',
                },
                {
                    name: 'shop',
                }
            ],
        };
    },
    components: { 
        IconSvg 
    },
    methods: {
        toggleDropdown(){
            this.dropDownVisible = !this.dropDownVisible
        },
        keepDropdown() {
            this.isDropdownVisible = true;
        },
        hideDropdown() {
            this.isDropdownVisible = false;
        },
    }
}
</script>

<template>

    <div class="head-page p-2 d-flex justify-content-between align-items-center">
            <!-- LOGO -->
            <div class="container-logo p-3">
                <figure>
                    <a href="#"><img src="../assets/logo.svg" alt="logo footer"></a>
                </figure>
            </div>

            <!-- NAVBAR -->
            <div>
                <nav>
                    <ul class="navbar-flex d-flex gap-5 my-2">
                        <li 
                        v-for="(element, index) in navLinks"
                        :key="index">
                            <a class="dropdown-toggle" data-bs-toggle="dropdown" href="#">{{ element.name }}</a>
                        </li>
                    </ul>
                </nav>
                
            </div>

            <!-- SOCIAL LINKS -->
            <div class="icons">

                <IconSvg>

                </IconSvg>


            </div>
        </div>
</template>

<style lang="scss" scoped>

.head-page{
    background-color: #ffffff;
    position: fixed;
    top: 0;
    width: 100%;
    overflow: hidden;
    z-index: 1;
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
            padding: 10px;
        }

        a:hover{
            background-color: black;
            color: white;
            padding: 10px;
        }
}
</style>