<script setup lang="ts">
import { ref } from "vue";
import MainPage from "./components/MainPage.vue";
import GoalsPage from "./components/GoalsPage.vue";
import MoneyPage from "./components/MoneyPage.vue";

const pageIndex = ref(0);
</script>

<template>
	<button @click="pageIndex = (pageIndex + 1) % 3">Change Page</button>
	<MainPage v-if="pageIndex === 0" />
	<GoalsPage v-else-if="pageIndex === 1" />
	<MoneyPage v-else />
</template>
