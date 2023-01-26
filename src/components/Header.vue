<script setup>
import { computed, ref } from '@vue/runtime-core';
import  {useRoute}  from 'vue-router'; 
const route = useRoute().path   
const navBar = ref()  

const active = computed(()=>{ 
    return {
        home: route == '/',
        about: route == '/about',
        service: route == '/service',
        work: route == '/work',
        blog: route == '/blog',
        contact: route == '/contact',
    }
})
</script>
<template>
    <div class="header container">

        <div class="logo">TECHLAMB</div>

        <div class="nav-bar" id="navBar" ref="navBar">
            <RouterLink to="/" > <div class="nav-item">HOME</div></RouterLink>
            <RouterLink to="/about"> <div class="nav-item">ABOUT</div></RouterLink>
            <RouterLink to="/service"><div class="nav-item"> SERVICES</div></RouterLink>
            <RouterLink to="/work"><div class="nav-item">WORK</div></RouterLink>
            <RouterLink to="/blog"><div class="nav-item">BLOG</div></RouterLink>
            <RouterLink to="/contact"><div class="nav-item">CONTACT</div></RouterLink>
        </div>
    </div>
</template> 