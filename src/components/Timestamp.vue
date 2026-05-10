<template>
  <span class="timestamp">{{ time }}</span>
</template>

<script setup>
defineProps({
  time: String,
});
</script>
