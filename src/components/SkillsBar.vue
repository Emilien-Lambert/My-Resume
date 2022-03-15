<script setup>
defineProps({
  title: {
    type: String,
    default: "mySkills",
  },
  datas: {
    type: Array,
    default: () => [
      {
        skillName: "",
        skillValue: 0,
      },
    ],
  },
});
</script>

<template>
  <div class="w-full">
    <div>
      <div class="text-xl font-bold text-purple-600">{{ title }}</div>
      <div class="w-20 h-1.5 bg-purple-600 my-3 rounded-full" />
    </div>
    <div class="grid grid-cols-3 gap-5">
      <div
        v-for="(data, dataIndex) in datas"
        :key="dataIndex"
        class="flex items-center justify-between"
      >
        <div
          class="text-center font-bold text-indigo-600 whitespace-nowrap w-4/12"
        >
          {{ data.skillName }}
        </div>
        <div class="w-full h-2 bg-gray-300 rounded-full">
          <div
            :style="`width: ${data.skillValue}%`"
            class="h-2 bg-purple-600 rounded-full"
          />
          <div class="mt-1 text-indigo-300">{{ data.quaterValue }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style></style>
