<script setup>
import { computed } from "vue";

const birthday = "08/01/1994";

const age = computed(() => {
  return new Date().getFullYear() - new Date(birthday).getFullYear();
});
</script>

<template>
  <div
    class="flex py-6 justify-around items-center text-white bg-gradient-to-br from-purple-900 to-cyan-200"
  >
    <img
      alt="profile picture"
      class="rounded-full w-2/12"
      src="/src/assets/profile1.jpeg"
    />
    <div class="flex flex-col w-1/2 justify-center">
      <div>
        <div class="text-5xl font-bold">Emilien Lambert</div>
        <div>Développeur informatique</div>
      </div>
      <div class="w-1/3 h-2 bg-white my-3 rounded-full" />
      <div class="grid grid-cols-2 gap-3">
        <div>
          <span>✉️ </span>
          <a href="mailto:lee-kewpie.0l@icloud.com" itemprop="email"
            >lee-kewpie.0l@icloud.com</a
          >
        </div>
        <div>
          <span>🎂 {{ age }} ans</span>
        </div>
        <div>
          <span>📞 06 74 27 22 43</span>
        </div>
        <div>
          <span>🎟 Permis A, B</span>
        </div>
        <div class="flex">
          🏠 
          <div class="flex flex-col">
            <div>25 Avenue Du Bois Chatel</div>
            <div>54270 Essey-Les-Nancy</div>
          </div>
        </div>
        <div>
          <span>🚗 Véhicule personnel</span>
        </div>
      </div>
    </div>
    <lottie-player
      autoplay
      background="transparent"
      loop
      speed="1"
      src="https://assets4.lottiefiles.com/packages/lf20_kyu7xb1v.json"
      style="width: 200px; height: 200px"
    ></lottie-player>
  </div>
</template>

<style></style>
