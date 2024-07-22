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

useSeoMeta({
    title: 'About',
    description: 'This is the About page',
    ogTitle: 'About',
    ogDescription: 'This is the About page',
    ogImage: 'https://example.com/image.png',
    ogUrl: '[og:url]',
    twitterTitle: 'About',
    twitterDescription: '[twitter:description]',
    twitterImage: '[twitter:image]',
    twitterCard: 'summary'
})
useHead({
    htmlAttrs: {
        lang: 'en'
    },
    link: [
        {
            rel: 'icon',
            type: 'image/png',
            href: '/favicon.png'
        }
    ]
})
</script>