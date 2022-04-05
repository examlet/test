<script lang="ts" setup>
const msg = ref('')
const kek = () => {
  fetch('http://quicksales.online/aps/')
  .then((response) => {
    return response.json();
  })
  .then((data) => {
    console.log(data);
    msg.value = data
  });
} 
</script>

<template>
  <div>
    {{ msg }}
    <button @click="kek">kek</button>
  </div>
</template>
