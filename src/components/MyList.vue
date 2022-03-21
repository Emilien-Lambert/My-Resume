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
        firstDate: "",
        secondDate: "",
        firstValue: "",
        secondValue: "",
        thirdValue: "",
        fourthValue: "",
      },
    ],
  },
});
</script>

<template>
  <div class="w-4/12">
    <div>
      <div class="text-xl font-bold text-purple-600">{{ $t(title) }}</div>
      <div class="w-20 h-1.5 bg-purple-600 my-3 rounded-full" />
    </div>
    <div v-for="(data, dataIndex) in datas" :key="dataIndex" class="flex my-5">
      <div
        v-if="
          ['Diplôme et Formations', 'Expériences professionnelles'].includes(
            title
          )
        "
        class="gap-2 w-1/4 text-lg text-cyan-400"
      >
        <div>De {{ data.firstDate }} à {{ data.secondDate }}</div>
      </div>
      <div class="w-3/4">
        <div class="font-bold text-indigo-600">
          {{ $t(data.firstValue) }}
        </div>
        <div class="text-purple-500">
          {{ $t(data.secondValue) }}
          <span class="text-indigo-500">{{ $t(data.thirdValue) }}</span>
        </div>
        <div class="mt-1 text-indigo-300">{{ $t(data.fourthValue) }}</div>
      </div>
    </div>
  </div>
</template>

<style></style>
