<template>
    <div>
        <div>Projects</div>

        <section v-if="pending">Loading...</section>
        <section v-else-if="error">Something went wrong... Try again!</section>
        <section v-else>
            <ul v-for="repository in repos" :key="repository.id"
                class="border border-gray-200 rounded-sm p-4 hover:bg-gray-100 font-mono">
                <a :href="repository.html_url" target="_blank">
                    <div class="flex items-center justify-between">
                        <div class="font-semibold">{{ repository.name }}</div>
                        <div>{{ repository.stargazers_count }} *</div>
                    </div>
                </a>
            </ul>
        </section>
    </div>
</template>

<script setup>
const { error, pending, data } = await useFetch('https://api.github.com/users/MinKhantNaung/repos')

const repos = computed(() => {
    return data.value.sort((a, b) => b.stargazers_count - a.stargazers_count)
})
</script>