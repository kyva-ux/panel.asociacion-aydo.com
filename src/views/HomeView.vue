<script setup>
import Calendar from '@/components/Calendar.vue'
</script>

<template lang="pug">
main
  .present
  .bookings
  .schedule
    Calendar
</template>

<style scoped>
main {
  display: grid;
  grid-template-areas:  "p s"
                        "b s";
  grid-template-columns: 60%;
  /* grid-template-rows: 400px; */
  gap: 2px;
  width: 100vw;
  height: 100vh;
}
.present {
  background: rgba(164, 170, 208, 0.1);
  grid-area: p;
}
.bookings {
  background: rgba(164, 170, 208, 0.05);
  grid-area: b;
}
.schedule {
  background: rgba(164, 170, 208, 0.15);
  grid-area: s;
}
</style>
