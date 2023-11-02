<template>
  <div class="reason-content mt-[100px] relative" id="reason">
    <img src="../assets/images/pattern2.png" alt="" class="absolute top-0 -left-[8%] xd:inline-block hidden">
    <Title class="text-center sm:my-8 my-5" >Почему Coozin?</Title>
    <div class="reasons">
        <div class="sm:grid grid-cols-3 gap-4 text-center flex flex-col">
            <div v-for="info in infos" :key="info.id" class="">
                <div class="img-wrapper w-[140px] h-[140px] flex items-center justify-center mx-auto">
                    <img :src="info.img" alt="" class="mx-auto">
                </div>
                <h2 class="font-bold text-slate-900 my-3">{{ info.title }}</h2>
                <p class="text-slate-700">{{ info.description }}</p>
            </div>
        </div>
    </div>
  </div>
</template>
<script>
import { Title, Description } from '../ui-components';
export default {

  components: {Title, Description},
  data() {
    return {
      infos: [
        {
          id: 1,
          title: "Универсальная платформа",
          description:
            "Предназначенная для самозанятых женщин превратить свое хобби в прибыльный бизнес",
          img: "/assets/img/rocket.png",
        },
        {
          id: 2,
          title: "Обучение и бизнес",
          description:
            "Женщины экономят время и ресурсы, которые могут быть направлены на развитие своего бизнеса",
          img: "/assets/img/business.png",
        },
        {
          id: 3,
          title: "Дополнительный заработок",
          description:
            "Домохозяйки могут стать партнерами нашего проекта и получить инструменты для управления своим бизнесом.",
          img: "/assets/img/coins.png",
        },
      ],
    };
  },
};
</script>
<style>
</style>