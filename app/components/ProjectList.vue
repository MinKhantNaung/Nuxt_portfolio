<template>
    <div>
        <div>Projects</div>

        <section v-if="pending">Loading...</section>
        <section v-else-if="error">Something went wrong... Try again!</section>
        <section v-else>Here we display the repos!</section>
    </div>
</template>

<script setup>
const { error, pending, data } = await useFetch('https://api.github.com/users/MinKhantNaung/repos')
</script>