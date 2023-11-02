<template>
  <label v-if="label" class="text-slate-600" :for="label">{{ label }}</label>
  <input
    type="text"
    :id="label"
    :value="value"
    class="px-4 py-3 outline-none rounded-lg w-full border border-slate-300"
  />
</template>
<script>
export default {
  props: {
    label: {
      type: String,
    },
    value: {
      type: String | Number,
    },
  },
};
</script>
<style>
</style>