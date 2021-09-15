<template>
    <div class="z-40 fixed bg-white w-full">
        <div class="w-full md:grid grid-cols-5 gap-3 shadow md:px-24 px-8 py-4 flex justify-between items-center">
            <div id="menu" class="md:hidden cursor-pointer ml-auto">
                <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
            </div>
            <router-link to="/">
                <div class="md:col-span-1">
                    <img class="w-1/4 md:w-16 ml-auto md:ml-0" src="../assets/images/logo.png" alt="Ameccad logo">
                </div>
            </router-link>
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
                <a href="{{ route('homepage') }}" class="flex justify-between items-center">
                    <span>Home</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-home text-3xl"></i></span>
                </a>
            </li>
            <hr>
            <li class="py-3 px-8" id="phone_nav_caret">
                <a href="#" class="flex justify-between items-center">
                    <span>Register</span>
                    &nbsp;&nbsp;
                    <span><svg class="w-8 h-8" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6 6V5a3 3 0 013-3h2a3 3 0 013 3v1h2a2 2 0 012 2v3.57A22.952 22.952 0 0110 13a22.95 22.95 0 01-8-1.43V8a2 2 0 012-2h2zm2-1a1 1 0 011-1h2a1 1 0 011 1v1H8V5zm1 5a1 1 0 011-1h.01a1 1 0 110 2H10a1 1 0 01-1-1z" clip-rule="evenodd"></path><path d="M2 13.692V16a2 2 0 002 2h12a2 2 0 002-2v-2.308A24.974 24.974 0 0110 15c-2.796 0-5.487-.46-8-1.308z"></path></svg></span>
                </a>
            </li>
            <div id="phone_nav_caret_menu" class="hidden absolute w-full px-4 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5">
                <div class="py-1 text-gray-700 list-none" aria-orientation="vertical">
                    <span class="user-setting-caret"><li><a href="{{ route('register') }}">Student</a></li></span>
                    <span class="user-setting-caret"><li><a href="{{ route('examiner') }}">Examiner</a></li></span>
                </div>
            </div>
            <hr>
            <li class="py-3 px-8">
                <a href="#" class="flex justify-between border-b-1 items-center">
                    <span>Check Results</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-dot-circle text-3xl"></i></span>
                </a>
            </li>
            <hr>
            <li class="py-3 px-8">
                <a href="{{ route('login') }}" class="flex justify-between items-center">
                    <span>Login</span>
                    &nbsp;&nbsp;
                    <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 3a1 1 0 011 1v12a1 1 0 11-2 0V4a1 1 0 011-1zm7.707 3.293a1 1 0 010 1.414L9.414 9H17a1 1 0 110 2H9.414l1.293 1.293a1 1 0 01-1.414 1.414l-3-3a1 1 0 010-1.414l3-3a1 1 0 011.414 0z" clip-rule="evenodd"></path></svg>
                </a>
            </li>
            <hr>
            <li class="py-3 px-8">
                <a href="#" class="flex justify-between items-center">
                    <span>About Us</span>
                    &nbsp;&nbsp;
                    <span><i class="fas fa-home text-3xl"></i></span>
                </a>
            </li>
            <hr>
            <li class="py-3 px-8">
                <a href="{{ route('contact') }}" class="flex justify-between items-center">
                    <span>Contact Us</span>
                    &nbsp;&nbsp;
                    <span><svg class="w-8 h-8" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"></path></svg></span>
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
