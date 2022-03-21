<script setup>
import { computed } from "vue";
// import MySwitch from "@/components/MySwitch.vue";

const birthday = "08/01/1994";

const age = computed(() => {
  return new Date().getFullYear() - new Date(birthday).getFullYear();
});
</script>

<template>
  <div
    class="flex justify-around items-center py-6 text-white bg-gradient-to-br from-purple-900 to-cyan-200"
  >
    <img
      alt="profile picture"
      class="w-2/12 rounded-full"
      src="/src/assets/profile.jpeg"
    />
    <div class="flex flex-col justify-center w-1/2">
      <div>
        <div class="text-5xl font-bold">Emilien Lambert</div>
        <div>{{ $t("header_subtitle") }}</div>
      </div>
      <div class="my-3 w-1/3 h-2 bg-white rounded-full" />
      <div class="grid grid-cols-2 gap-3">
        <div>
          <span class="mx-2">✉️</span>
          <a href="mailto:lee-kewpie.0l@icloud.com" itemprop="email"
            >lee-kewpie.0l@icloud.com</a
          >
        </div>
        <div>
          <span class="mx-2">🎂</span>
          <span>{{ age }} {{ $t("years_old") }}</span>
        </div>
        <div>
          <span class="mx-2">📞</span>
          <span>06 74 27 22 43</span>
        </div>
        <div>
          <span class="mx-2">🎟</span>
          <span>{{ $t("driver's_license") }}</span>
        </div>
        <div class="flex">
          <span class="mx-2">🏠</span>
          <div class="flex flex-col">
            <div>25 Avenue Du Bois Chatel</div>
            <div>54270 Essey-Les-Nancy</div>
          </div>
        </div>
        <div>
          <span class="mx-2">🚗</span>
          <span>{{ $t("personal_vehicle") }}</span>
        </div>
      </div>
    </div>
    <div class="flex flex-col items-center">
      <lottie-player
        autoplay
        background="transparent"
        loop
        speed="1"
        src="https://assets4.lottiefiles.com/packages/lf20_kyu7xb1v.json"
        style="width: 200px; height: 200px"
      ></lottie-player>
      <!--      <MySwitch />-->
    </div>
  </div>
</template>

<style></style>
