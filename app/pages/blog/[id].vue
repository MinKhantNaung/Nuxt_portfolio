<template>
    <div>
        You are inside a blog.
        <h1>This is id - {{ route.params.id }}</h1>
    </div>
</template>

<script setup>
const route = useRoute();

</script>