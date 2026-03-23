<template>
  <div class="page-container">
    <h2>📋 Summary</h2>
    <!-- TODO: ดึง username และ favorites.length จาก store -->
    <p v-if="store.username">ชื่อผู้ใช้: {{ store.username }}</p>
    <p v-else>ชื่อผู้ใช้: -</p>
    <p>จำนวนคอร์สที่ถูกใจ: {{ store.favorites.length }}</p>
  </div>
</template>

<script setup>
// TODO: import { useFavoriteStore }
import { useFavoriteStore } from "../stores/favorite";

const store = useFavoriteStore();
</script>

<style scoped>
.page-container {
  text-align: center;
  padding: 40px;
}
</style>
