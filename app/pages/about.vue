<template>
    <div>
        This is about me.

        <button @click="enableCustomLayout">Update layout</button>
    </div>
</template>

<script setup>
function enableCustomLayout() {
    setPageLayout('another')
}
</script>