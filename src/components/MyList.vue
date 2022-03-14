<script setup>
defineProps({
  title: {
    type: String,
    default: "myTitle",
  },
  datas: {
    type: Array,
    default: () => [
      {
        date: "date - date",
        firstValue: "firstValue",
        secondValue: "secondValue",
        thirdValue: "thirdValue",
      },
    ],
  },
});
</script>

<template>
  <div class="w-4/12">
    <div>
      <div class="text-xl font-bold text-purple-600">{{ title }}</div>
      <div class="w-2/12 h-1.5 bg-purple-600 my-3 rounded-full" />
    </div>
    <div
      v-for="(data, dataIndex) in datas"
      :key="dataIndex"
      class="flex gap-12 my-5"
    >
      <div class="text-lg text-cyan-400">
        <div class="whitespace-nowrap">De {{ data.firstDate }}</div>
        <div class="whitespace-nowrap">à {{ data.secondDate }}</div>
      </div>
      <div>
        <div class="text-indigo-600 font-bold">
          {{ data.firstValue }}
        </div>
        <div class="text-purple-500">
          {{ data.secondValue }}
          <span class="text-indigo-500">{{ data.thirdValue }}</span>
        </div>
        <div class="mt-1 text-indigo-300">{{ data.quaterValue }}</div>
      </div>
    </div>
  </div>
</template>

<style></style>
