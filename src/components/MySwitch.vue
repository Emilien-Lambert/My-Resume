<script setup>
import { ref } from "vue";
import { Switch } from "@headlessui/vue";
import { useI18n } from "vue-i18n";

const { locale } = useI18n();
const enabled = ref(false);

const changeLocale = () => {
  locale.value = locale.value === "fr" ? "en" : "fr";
};
</script>

<template>
  <div class="inline-flex gap-3 items-center">
    {{ locale.value }}
    <span>Français</span>
    <Switch
      v-model="enabled"
      :class="[
        enabled ? 'bg-purple-600' : 'bg-gray-200',
        'relative inline-flex flex-shrink-0 h-6 w-11 border-2 border-transparent rounded-full cursor-pointer transition-colors ease-in-out duration-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500',
      ]"
      @click="changeLocale"
    >
      <span
        :class="[
          enabled ? 'translate-x-5' : 'translate-x-0',
          'pointer-events-none inline-block h-5 w-5 rounded-full bg-white shadow transform ring-0 transition ease-in-out duration-200',
        ]"
        aria-hidden="true"
      />
    </Switch>
    <span>English</span>
  </div>
</template>
