<template>
    <div>
        This is home page.
    </div>
</template>

<script setup>
useSeoMeta({
    title: 'Main Page',
    description: 'This is the main page',
    ogTitle: 'Main Page',
    ogDescription: 'This is the main page',
    ogImage: 'https://example.com/image.png',
    ogUrl: '[og:url]',
    twitterTitle: 'Main Page',
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