<script>
    import AppHeader from './components/AppHeader.vue'
    import AppMain from './components/AppMain.vue'
    import AppFooter from './components/AppFooter.vue'

    export default {
        components:{
            AppHeader,
            AppMain,
            AppFooter
        }
    }

</script>

<template>
<header>
    <AppHeader></AppHeader>
</header>

<main>
    <AppMain></AppMain>
</main>

<footer>
    <AppFooter></AppFooter>
</footer>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
*{
    font-family: 'Poppins', sans-serif;
}

</style>
