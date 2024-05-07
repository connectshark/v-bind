<template>
  <td>{{ name }}</td>
  <td>{{ occupation }}</td>
  <td>{{ email }}</td>
</template>

<script setup>
defineProps({
  name: String,
  occupation: String,
  email: String
})
</script>