<script setup>
import { RouterLink, RouterView, useRoute } from 'vue-router'  
import FooterVue from './components/Footer.vue';
import HeaderVue from './components/Header.vue'; 
</script>

<template> 
<div class="main-container">
    <HeaderVue />
    <RouterView />
    <FooterVue />
     </div>
</template>
