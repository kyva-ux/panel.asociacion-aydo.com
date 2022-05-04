<script setup>
import { ref, computed } from 'vue'
import { DatePicker } from 'v-calendar'
import 'v-calendar/dist/style.css'

const date = ref(new Date())

const attrs = computed(() => {
  return [
    {
      key: 'today',
      highlight: {
        color: 'purple',
        fillMode: 'outline',
      },
      dates: new Date(),
    },
    ...todos.map(todo => ({
      dates: todo.dates,
      dot: todo.color,
      popover: {
        label: todo.description,
      },
      customData: todo,
    })),
  ];
})
const todos = [
  {
    description: '9:00 a 12:00',
    isComplete: false,
    dates: { weekdays: 6 }, // Every Friday
    color: 'green',
  },
]
</script>

<template lang="pug">
.date-picker
  DatePicker(
    v-model="date"
    :firstDayOfWeek="2"
    locale="es"
    dayNames
    is-dark
    color="purple"
    :min-date="new Date()"
    :attributes='attrs'
  )
  p Date: {{ date.toJSON() }}
</template>

<style scoped>
</style>
