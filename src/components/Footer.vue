<template>
  <div class="footer-content sm:mt-[120px] mt-14 mb-10">
    <div class="footer-box flex flex-col items-center">
        <img src="../assets/icons/logo-footer.svg" alt="">

        <ul class="sm:flex sm:flex-row flex-col mt-12 hidden">
                <li class="mx-2 py-1 px-1 cursor-pointer text-gray-700 font-normal" v-for="link in links" :key="link.id"><a :href="link.target">{{ link.label }}</a></li>    
        </ul>

        <div class="mt-8 sm:flex hidden justify-between gap-10">
            <h3 class="text-gray-900">При поддержке</h3>
            <img src="../assets/icons/cola.svg" alt="">
            <img src="../assets/icons/osce.svg" alt="">
        </div>
        <div class="mt-8 flex justify-between items-center sm:gap-10 gap-6">
            <h3 class="text-gray-900 sm:block hidden">ПОДПИСЫВАЙТЕСЬ HA HAC</h3>
            <div class="line w-[70px] h-[1px] bg-gray-600 sm:block hidden"></div>
            <a href="http://instagram.com"><i class="text-xl text-gray-900 rounded-full sm:w-12 sm:h-12 w-10 h-10 text-center items-center flex justify-center border-slate-900 cursor-pointer border fa-brands fa-instagram"></i></a>
            <a href="http://facebook.com"><i class="text-xl text-gray-900 rounded-full sm:w-12 sm:h-12 w-10 h-10 text-center items-center flex justify-center border-slate-900 cursor-pointer border fa-brands fa-facebook"></i></a>
            <a href="http://youtube.com"><i class="text-xl text-gray-900 rounded-full sm:w-12 sm:h-12 w-10 h-10 text-center items-center flex justify-center border-slate-900 cursor-pointer border fa-brands fa-youtube"></i></a>
        </div>

        <p class="mt-8 sm:text-base text-sm text-gray-800">2023 Coozin. All Rights Reserved</p>
    </div>
  </div>
</template>
<script>
// О нас Edu Coozin Почему Coozin? Присоединиться Мероприятия
export default {
    data() {
        return {
            links: [
                {id: 1, label: 'O нас', target: '#about'},
                {id: 2, label: 'Edu Coozin', target: '#education'},
                {id: 3, label: 'Почему Coozin?', target: '#reason'},
                {id: 4, label: 'Присоединиться', target: '#join'},
                {id: 5, label: 'Мероприятия', target: '#events'},
            ],
        }
    }
};
</script>
<style>
</style>