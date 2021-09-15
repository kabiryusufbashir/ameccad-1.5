<template>
    <div class="z-40 fixed bg-white w-full">
        <div class="bg-white w-full md:grid grid-cols-5 gap-3 shadow md:px-24 px-8 py-4 flex justify-between items-center text-black">
            <div id="menu" class="md:hidden cursor-pointer ml-auto">
                <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
            </div>
            <a href="/">
                <div class="md:col-span-1">
                    <img class="w-1/4 md:w-16 ml-auto md:ml-0" src="../assets/images/logo.png" alt="AMECCAD logo">
                </div>
            </a>
            <div class="md:col-span-3 md:relative hidden md:block uppercase">
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
                    <li><a href="#">Contact Us</a></li>
                </nav>
            </div>
        </div>
    </div>
    <!-- Mobile Nav -->
    <div id="nav" class="w-full fixed h-screen z-30 hidden bg-white py-8">
        <div class="list-none p-2 text-xl border-t bg-white pt-20">
            <li class="py-3 px-8">
                <a href="{{ route('homepage') }}" class="flex justify-between items-center">
                    <span>Home</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-home text-3xl"></i></span>
                </a>
            </li>
            <hr>
            <li class="py-3 px-8">
                <a href="#" class="flex justify-between border-b-1 items-center">
                    <span>About Us</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-dot-circle text-3xl"></i></span>
                </a>
            </li>
            <hr>
            <li class="py-3 px-8">
                <a href="#" class="flex justify-between border-b-1 items-center">
                    <span>Courses</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-dot-circle text-3xl"></i></span>
                </a>
            </li>
            <hr>
            <li class="py-3 px-8">
                <a href="#" class="flex justify-between border-b-1 items-center">
                    <span>Our Team</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-dot-circle text-3xl"></i></span>
                </a>
            </li>
            <hr>
            <li class="py-3 px-8">
                <a href="#" class="flex justify-between border-b-1 items-center">
                    <span>Contact Us</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-dot-circle text-3xl"></i></span>
                </a>
            </li>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'Nav',
    } 
</script>
