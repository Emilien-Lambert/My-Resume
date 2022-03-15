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
        firstDate: "firstDate",
        secondDate: "secondDate",
        firstValue: "firstValue",
        secondValue: "secondValue",
        thirdValue: "thirdValue",
        quaterValue: "quaterValue",
      },
    ],
  },
});
</script>

<template>
  <div class="w-4/12" style="border: solid 1px red">
    <div>
      <div class="text-xl font-bold text-purple-600">{{ title }}</div>
      <div class="w-2/12 h-1.5 bg-purple-600 my-3 rounded-full" />
    </div>
    <div v-for="(data, dataIndex) in datas" :key="dataIndex" class="flex my-5">
      <div
        v-if="
          ['Diplôme et Formations', 'Expériences professionnelles'].includes(
            title
          )
        "
        class="text-lg text-cyan-400 w-1/4"
      >
        <div>De {{ data.firstDate }} à {{ data.secondDate }}</div>
      </div>
      <div class="w-3/4">
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
