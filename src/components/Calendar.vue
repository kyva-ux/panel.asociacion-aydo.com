<script setup>
import { ref } from 'vue'
import { DatePicker } from 'v-calendar'
import 'v-calendar/dist/style.css'

const date = ref(new Date)
</script>

<template lang="pug">
.calendar
  div Hi from calendar
  //- DatePicker
</template>

<style lang="sass" scoped>
</style>
