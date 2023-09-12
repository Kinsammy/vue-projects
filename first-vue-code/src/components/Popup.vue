<template>
  <h2>This is Popup Event</h2>
  <button @click="$emit('close', 'Samuel')">Close Popup Event</button>
</template>

<script>
export default {
  name: "Popup",
  emits: ["close"],
};
</script>

<style scoped></style>
