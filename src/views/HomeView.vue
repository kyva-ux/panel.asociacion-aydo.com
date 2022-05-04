<script setup>
import DatePicker from '@/components/DatePicker.vue'
</script>

<template lang="pug">
main
  .calendar
    .title Calendario
  .bookings
    .title Reservas
  .schedule
    .title Días y horas disponibles
    DatePicker
</template>

<style scoped>
main {
  display: grid;
  grid-template-areas:  "p s"
                        "b s";
  grid-template-columns: 60%;
  grid-template-rows: 50vh;
  gap: 2px;
  width: 100vw;
  height: 100vh;
}
.calendar {
  background: rgba(164, 170, 208, 0.1);
  grid-area: p;
  padding-top: 40px;
}
.bookings {
  background: rgba(164, 170, 208, 0.05);
  grid-area: b;
  padding-top: 40px;
}
.schedule {
  background: rgba(164, 170, 208, 0.15);
  grid-area: s;
  padding-top: 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.title {
  text-align: center;
  display: block;
  font-size: 24px;
  margin-bottom: 40px;
}
</style>
