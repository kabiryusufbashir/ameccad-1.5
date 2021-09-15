<template>
    <div class="z-40 fixed bg-white w-full">
        <div class="w-full md:grid grid-cols-5 gap-3 shadow md:px-24 px-8 py-4 flex justify-between items-center">
            <router-link to="/">
                <div class="md:col-span-1">
                    <img class="w-2/4 md:w-16 md:ml-0" src="../assets/images/logo.png" alt="Ameccad logo">
                </div>
            </router-link>
            <div id="menu" @click="showMenu()" class="md:hidden cursor-pointer ml-auto">
                <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
            </div>
            <div class="md:col-span-4 md:relative hidden md:block uppercase">
                <nav class="md:flex justify-between list-none">
                    <li>
                        <router-link to="/">Home</router-link>
                    </li>
                    <li>
                        <router-link to="/about">About</router-link>
                    </li>
                    <li>
                        <router-link to="/courses">Courses</router-link>
                    </li>
                    <li>
                        <router-link to="/team">Our Team</router-link>
                    </li>
                    <li>
                        <router-link to="/contact">Contact Us</router-link>
                    </li>
                </nav>
            </div>
        </div>
    </div>
    <!-- Mobile Nav -->
    <div id="nav" class="w-full fixed h-screen z-30 hidden bg-white py-8">
        <div class="list-none p-2 text-xl border-t bg-white pt-20">
            <li class="py-3 px-8">
                <router-link to="/" class="flex justify-between items-center">
                    <span>Home</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-home text-3xl"></i></span>
                </router-link>
            </li>
            <hr>
            <li class="py-3 px-8" id="phone_nav_caret">
                <router-link to="/about" class="flex justify-between items-center">
                    <span>About Us</span>
                    &nbsp;&nbsp;
                    <span><svg class="w-8 h-8" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6 6V5a3 3 0 013-3h2a3 3 0 013 3v1h2a2 2 0 012 2v3.57A22.952 22.952 0 0110 13a22.95 22.95 0 01-8-1.43V8a2 2 0 012-2h2zm2-1a1 1 0 011-1h2a1 1 0 011 1v1H8V5zm1 5a1 1 0 011-1h.01a1 1 0 110 2H10a1 1 0 01-1-1z" clip-rule="evenodd"></path><path d="M2 13.692V16a2 2 0 002 2h12a2 2 0 002-2v-2.308A24.974 24.974 0 0110 15c-2.796 0-5.487-.46-8-1.308z"></path></svg></span>
                </router-link>
            </li>
            <hr>
            <li class="py-3 px-8">
                <router-link to="/courses" class="flex justify-between border-b-1 items-center">
                    <span>Courses</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-dot-circle text-3xl"></i></span>
                </router-link>
            </li>
            <hr>
            <li class="py-3 px-8">
                <router-link to="/team" class="flex justify-between items-center">
                    <span>Login</span>
                    &nbsp;&nbsp;
                    <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 3a1 1 0 011 1v12a1 1 0 11-2 0V4a1 1 0 011-1zm7.707 3.293a1 1 0 010 1.414L9.414 9H17a1 1 0 110 2H9.414l1.293 1.293a1 1 0 01-1.414 1.414l-3-3a1 1 0 010-1.414l3-3a1 1 0 011.414 0z" clip-rule="evenodd"></path></svg>
                </router-link>
            </li>
            <hr>
            <li class="py-3 px-8">
                <router-link to="/contact" class="flex justify-between items-center">
                    <span>Contact Us</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-home text-3xl"></i></span>
                </router-link>
            </li>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'Nav',
        methods:{
            showMenu(){
                let menu = document.querySelector('#menu');
                let nav = document.querySelector('#nav');

                menu.addEventListener('click', ()=>{
                    if(nav.classList.contains('hidden')){
                        nav.classList.remove('hidden');
                    }else{
                        nav.classList.add('hidden');
                    }
                });
            }
        }
    } 
</script>
