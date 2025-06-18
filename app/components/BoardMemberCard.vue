<script setup lang="ts">
interface BoardMemberCardProps {
  src: string
  name: string
  title: string
}

const {
  src,
  name,
  title
} = defineProps<BoardMemberCardProps>()
</script>

<template>
  <div class="">
    <UUser
      :name="name"
      class="items-center justify-center"
      orientation="vertical"
      :description="title"
      size="3xl"
      :avatar="{
        src: src,
        alt: name,
        icon: 'i-lucide-image'
      }"
    />
  </div>
</template>
