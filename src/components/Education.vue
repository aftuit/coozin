<template>
  <div  id="education" class="ss:grid grid-cols-2 ss:gap-[5rem] gap-[3.5rem] mt-[80px] flex flex-col">
    <div class="cols-span-1">
      <img src="../assets/images/img3.png" alt="" />
    </div>
    <div class="cols-span-1 sm:pe-10">
      <Title class="ss:mt-16">
        EDU COOZIN
      </Title>
      <Description>
        Онлайн-академия Coozin предоставляет обучение и помощь в развитии
        бизнеса.
      </Description>

      <div class="info">
        <div class="xd:mt-8 mt-4" :key="fac.id" v-for="fac in facilities">
          <div class="flex items-center text-slate-800 font-semibold ss:text-[20px] text-[18px]">
            <img src="../assets/icons/checkmark.svg" alt="" class="me-4" />
            {{fac.title}}
          </div>
          <Description class="ellipsis ss:hidden xd:block">
            {{fac.description}}
          </Description>
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
      facilities: [
        {
          id: 1,
          title: 'Курсы и мастер-классы',
          description: 'Ha платформе доступны онлайн-курсы и мастер-классы по различным темам, связанным c бизнесом, такими как управление продажами, маркетинг, финансы и другие',
        },
        {
          id: 2,
          title: 'Опытные специалисты',
          description: 'Курсы ведут опытные специалисты, которые делятся своими знаниями и опытом.',
        },
        {
          id: 3,
          title: 'Обучись и начни свое дело',
          description: 'Пользователи которые успешно прошли курсы имеют возможность присоединиться к торговой площадке Coozin.',
        },
      ]
    }
  }
};
</script>

<style scoped>
</style>