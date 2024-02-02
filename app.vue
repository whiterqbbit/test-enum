<template>
  <button @click="showEnum">Show enum</button>
  <div>
    RESPONSE : {{ resp }}
  </div>
</template>

<script setup>
const resp = ref(null)
async function showEnum() {
  resp.value = await $fetch('/api/test')
}
</script>