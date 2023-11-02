<template >
  <div class="flex flex-col">
    <label v-if="label" class="text-slate-600" :for="label">{{ label }}</label>
    <select :id="label" class="px-4 py-3 outline-none rounded-lg " :class="className">
      <option v-for="option in options" :value="option.value" :key="option.id">
        {{ option.value }}
      </option>
    </select>
  </div>
</template>
<script>
export default {
  props: {
    options: {
      type: Object,
      required: true,
    },
    label: {
      type: String,
    },
    className: {
      type: String,
    },
  },
};
</script>
<style scoped>
.select select{
  appearance: none;
}
</style>