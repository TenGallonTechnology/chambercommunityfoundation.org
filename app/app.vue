<script setup lang="ts">
useHead({
  meta: [{ name: 'viewport', content: 'width=device-width, initial-scale=1' }],
  link: [{ rel: 'icon', href: '/favicon.ico' }],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'Dublin-Laurens County Chamber Community Foundation'
const description
  = 'Uniting community leaders to build a stronger future through childcare, education, and workforce solutions.'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: '/1.png',
  twitterImage: '/1.png',
  twitterCard: 'summary_large_image'
})

const route = useRoute()
const items = computed(() => [
  {
    label: 'About',
    to: '/#about',
    active: route.path.includes('/#about')
  },
  {
    label: 'Board Members',
    to: '/#board-members',
    active: route.path.includes('/#board-members')
  },
  {
    label: 'Childcare',
    to: '/#childcare',
    active: route.path.includes('/#childcare')
  },
  {
    label: 'Donate',
    to: '/#donate',
    active: route.path.includes('/#donate')
  },
  {
    label: 'Education',
    to: '/#education',
    active: route.path.includes('/#education')
  },
  {
    label: 'Workforce',
    to: '/#workforce',
    active: route.path.includes('/#workforce')
  }
])
</script>

<template>
  <UApp>
    <UHeader mode="drawer">
      <template #title>
        <img
          src="/2-transparent.png"
          class="w-auto h-15 shrink-0"
        >
      </template>
      <UNavigationMenu :items="items" />
      <template #body>
        <UNavigationMenu
          :items="items"
          orientation="vertical"
          class="-mx-2.5"
        />
      </template>
    </UHeader>

    <UMain>
      <NuxtPage />
    </UMain>

    <USeparator />

    <UFooter>
      <template #left>
        <p class="text-sm text-muted">
          Copyright © {{ new Date().getFullYear() }}
        </p>
      </template>

      <template #right>
        <UButton
          to="https://tengallontechnology.com"
          target="_blank"
          :ui="{
            leadingAvatarSize: 'lg'
          }"
          :avatar="{
            src: 'https://raw.githubusercontent.com/TenGallonTechnology/images/refs/heads/main/tenGallonSolid.png'
          }"
          color="neutral"
          variant="ghost"
        />
      </template>
    </UFooter>
  </UApp>
</template>
