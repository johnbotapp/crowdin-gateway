<template>
  <div>
    <span>An error occurred: {{ error }}</span>
  </div>
</template>

<script setup>
  defineProps({
    error: {
      type: Object,
      required: true
    }
  });

</script>
