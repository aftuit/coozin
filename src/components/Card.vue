<template >
  <div class="content sm:mt-0 mt-5">
    <div class="card p-8 text-center bg-slate-100">
      <img src="../assets/icons/quotes.svg" alt="" class="mx-auto" />
      <p class="mt-4 text-slate-700">{{ user.description }}</p>
      <i class="fa-solid fa-caret-down bottom-arrow text-4xl"></i>
    </div>
    <div class="user mx-auto mt-8">
      <div class="avatar w-full text-center">
        <img :src="user.avatar" alt="" class="mx-auto" />
        <h4 class="font-semibold my-1 mb-0">{{ user.name }}</h4>
        <span>{{ user.job }}</span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    user: {
      type: Object,
      required: true,
    },
  },
};
</script>
<style scoped>
.card {
  position: relative;
}
.bottom-arrow {
  position: absolute;
  color: #f3f4f6;
  bottom: -22px;
}
</style>