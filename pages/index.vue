<template>
    tst aaaa
</template>

<script setup>
useSeoMeta({
  title: 'Main page',
  description: 'This is the main page',
  ogTitle: 'Main page',
  ogDescription: 'This is the main page',
  ogImage: 'https://random.dog/f5b589f6-923b-44ef-9051-537c61b5a34f.jpg',
  ogUrl: '[og:url]',
  twitterTitle: '[twitter:title]',
  twitterDescription: '[twitter:description]',
  twitterImage: 'https://random.dog/f5b589f6-923b-44ef-9051-537c61b5a34f.jpg',
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