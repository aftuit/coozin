<template>
  <div class="comments-wrap mt-[100px]">
    <Title class="text-center">Наши довольные вендоры</Title>
    <div class="sm:grid sm:grid-cols-3 gap-4 mt-12 flex flex-col">
      <Card v-for="user in users" :key="user.id" :user="user"/>
    </div>
  </div>
</template>
<script>
import { Title } from "../ui-components";
import Card from "./Card.vue";
export default {
  components: {
    Title,
    Card,
  },
  data() {
    return {
      users: [
        {
          id: 1,
          avatar: "/assets/img/user1.png",
          name: "Lucy",
          job: "Designer",
          description:
            "When our designs need an expert opinion or approval, I know I can rely on your agency Thank you for all your help-I will be recommending you to everyone",
        },
        {
          id: 2,
          avatar: "/assets/img/user2.png",
          name: "Anna",
          job: "Programmer",
          description:
            "When our designs need an expert opinion or approval, I know I can rely on your agency Thank you for all your help-I will be recommending you to everyone",
        },
        {
          id: 3,
          avatar: "/assets/img/user3.png",
          name: "Alice",
          job: "Teacher",
          description:
            "When our designs need an expert opinion or approval, I know I can rely on your agency Thank you for all your help-I will be recommending you to everyone",
        },
      ],
    };
  },
};
</script>
<style scoped>
</style>