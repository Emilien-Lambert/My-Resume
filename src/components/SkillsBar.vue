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
      <div class="text-xl font-bold text-purple-600">{{ $t(title) }}</div>
      <div class="inline-flex items-center text-indigo-500">
        {{ $t("more_details") }}
        <a href="https://github.com/Emilien-Lambert" target="_blank">
          <img alt="logo GitHub" class="w-20" src="/src/assets/github.png" />
        </a>
      </div>
      <div class="w-20 h-1.5 bg-purple-600 my-3 rounded-full" />
    </div>
    <div class="grid grid-cols-3 gap-5">
      <div
        v-for="(data, dataIndex) in datas"
        :key="dataIndex"
        class="flex gap-2 justify-between items-center"
      >
        <div
          class="w-4/12 font-bold text-center text-indigo-600 whitespace-nowrap"
        >
          {{ $t(data.skillName) }}
        </div>
        <div class="w-full h-2 bg-gray-300 rounded-full">
          <div
            :style="`width: ${data.skillValue}%`"
            class="relative h-2 bg-purple-600 rounded-full"
          >
            <iframe
              v-if="dataIndex === datas.length - 1"
              allowFullScreen
              class="absolute bottom-0 left-full"
              frameBorder="0"
              height="359"
              src="https://giphy.com/embed/tPKoWQJk3cEbC"
              width="480"
            ></iframe>
          </div>
          <div class="mt-1 text-indigo-300">{{ data.fourthValue }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style></style>
