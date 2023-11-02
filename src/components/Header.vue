<template >

  <div id="about" class="header-wrapper sm:grid flex grid-cols-2 gap-10 sm:pe-12 mt-12 md:flex-row flex-col-reverse">
    <div class=" text-left col-span-1 sm:mt-16 mt-5 flex flex-col justify-around">
      <div >
        <Title>Раскрой свой потенциал вместе c Coozin!</Title>
        <Description class="mt-6">
          Универсальная платформа Coozin предоставляют множество возможностей для
          самозанятых женщин. Ha платформе можно продавать товары и услуги, a
          также учиться новым навыкам и развивать свой бизнес
        </Description>
        <Button class="mt-6 sm:w-fit w-full">Присоединиться</Button>  
      </div>


      <div class="ratings mt-10 sm:block hidden">
        <Description class=" font-semibold">Достижения</Description>

        <div class="grid grid-cols-3 gap-8 mt-10">
          <div class="col-span-1">
            <div class="rating-info">
              <h2 class="text-2xl font-bold text-gray-800">1K</h2>
              <Description>женщин прошли обучение</Description>
            </div>
          </div>
          <div class="col-span-1">
            <div class="rating-info">
              <h2 class="text-2xl font-bold text-gray-800">130K</h2>
              <Description>присоединились в платформу</Description>
            </div>
          </div>
          <div class="col-span-1">
            <div class="rating-info">
              <h2 class="text-2xl font-bold text-gray-800">1K</h2>
              <Description >пользователей платформы</Description>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="col-span-1">
        <div class="grid grid-cols-3 gap-5">
            <div class="col-span-2">
                <img src="../assets/images/img1.png" alt="" class="w-full h-full">
            </div>
            <div class="col-span-1">
                <img src="../assets/images/img4.png" alt="" class="w-full h-full">
            </div>
            <div class="col-span-1">
                <img src="../assets/images/img2.png" alt="" class="w-full h-full">
            </div>
            <div class="col-span-2">
                <img src="../assets/images/img5.png" alt="" class="w-full h-full">
            </div>
        </div>
    </div>
  </div>
</template>
<script>
import { Button, Title, Description} from '../ui-components';
export default {
    components: {Button, Title, Description}
};
</script>
<style scoped>
</style>