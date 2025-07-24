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
  <div
    data-orientation="vertical"
    class="relative group/user flex flex-col gap-3 items-center justify-center"
  >
    <span class="inline-flex items-center justify-center select-none overflow-hidden rounded-2xl align-middle bg-elevated size-20 text-2xl shrink-0"><img
      role="img"
      :src="src"
      :alt="name"
      class="h-full w-full object-cover"
      height="60"
      width="60"
    ></span><div class="">
      <p class="font-medium text-highlighted text-lg">
        {{ name }}
      </p>
      <p
        v-if="title"
        class="text-muted text-base"
      >
        {{ title }}
      </p>
    </div>
  </div>
</template>
