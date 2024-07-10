<template>
  <NuxtLayout :name="layout">
    <NuxtRouteAnnouncer />
    <NuxtPage />
  </NuxtLayout>
</template>

<script setup>
const layout = 'another';
</script>
