<template>
    <div class="nav-wrapper flex justify-between items-center py-4 sm:px-3 px-0"> 
        <div class="menu-bar sm:hidden flex justify-center items-center">
            <div 
            :class="isOpen? 'left-0': '-left-full'"
            class="nav-links fixed top-0 bottom-0 shadow-md z-10 bg-slate-50 transition-all ">
                <ul class="flex flex-col mt-16 p-5">
                    <button type="button" @click="showNavbar" class="absolute top-10 right-5 text-2xl text-slate-600"><i class="fa-solid fa-xmark"></i></button>
                    <li class="mt-4 py-1 px-2 cursor-pointer text-gray-700 font-normal" v-for="link in links" :key="link.id"><a :href="link.target">{{ link.label }}</a></li>
                </ul>
            </div>

            <div v-if="isOpen" class="shadow-box fixed top-0 bottom-0 right-0 left-0 backdrop-blur-sm transition-all z-[5]"></div>

            <button type="button" @click="showNavbar" class="border-none bg-none ss:p-3 m-auto">
                <img src="../assets/icons/menu.svg" alt="" class="w-[24px]">
            </button>
        </div>
        <div class="logo cursor-pointer">
            <img src='../assets/icons/logo.svg' alt="" class="xs:w-[150px] w-[100px]">
        </div>
            <ul class="sm:flex hidden min-w-[50%]">
                <li class="mx-2 py-1 px-1 cursor-pointer text-gray-700 font-normal" v-for="link in links" :key="link.id"><a :href="link.target">{{ link.label }}</a></li>    
            </ul>
            
           <div class="action-side flex ">
                <Select :options="languages" class="select" :className="'bg-gray-50 ss:me-4 select'"/>
                <Button class="md:inline-block hidden">Присоединиться</Button>
            </div>        
    </div>
</template>
<script>
import logo from "../assets/icons/logo.svg"
import { Select, Button } from "../ui-components";
export default {
    components: {
        Select,
        Button
    },
    data() {
        return {
            logo: logo,
            languages: [
                {id: 1, value: 'Uz'},
                {id: 2, value: 'Ru'},
                {id: 3, value: 'En'},
            ],
            links: [
                {id: 1, label: 'O нас', target: '#about'},
                {id: 2, label: 'Edu Coozin', target: '#education'},
                {id: 3, label: 'Почему Coozin?', target: '#reason'},
                {id: 4, label: 'Мероприятия', target: '#events'},
            ],
            isOpen: false,
        }
    },
    methods: {
        showNavbar() {
            this.isOpen = !this.isOpen
        }
    }
}
</script>
<style scoped>
    .select select{
        appearance: none;
}
</style>