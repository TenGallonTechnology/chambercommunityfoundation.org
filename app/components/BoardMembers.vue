<script setup lang="ts">
import BoardMemberCard from '~/components/BoardMemberCard.vue'

const boardMembers = [
  {
    src: '/board/sara-kolbie.jpg',
    name: 'Sara Kolbie',
    title: 'Director'
  },
  {
    src: '/board/joey-barrett.png',
    name: 'Joey Barret',
    title: 'Chair'
  },
  {
    src: '/board/kim-david.jpg',
    name: 'Kim David',
    title: 'Secretary'
  },
  {
    src: '/board/jeff-bruton.jpg',
    name: 'Jeff Bruton',
    title: 'Treasurer'
  },
  {
    src: '/board/lucas-cowart.jpg',
    name: 'Lucas Cowart',
    title: ''
  },
  {
    src: '/board/will-curry.jpg',
    name: 'Will Curry',
    title: ''
  },
  {
    src: '/board/marcia-dixon.jpg',
    name: 'Marcia Dixon',
    title: 'Dublin-Laurens Chamber of Commerce'
  },
  {
    src: '/board/randy-gay.jpg',
    name: 'Randy Gay',
    title: ''
  },
  {
    src: '/board/ben-lanier.jpg',
    name: 'Ben Lanier',
    title: ''
  },
  {
    src: '/board/michael-maffett.jpg',
    name: 'Michael Maffett',
    title: 'Curry-Maffett Insurance'
  },
  {
    src: '/board/randy-thompson.jpg',
    name: 'Randy Thompson',
    title: ''
  },
  {
    src: '/board/ronda-walker.png',
    name: 'Ronda Walker',
    title: ''
  }
]
</script>

<template>
  <UPageSection
    id="board-members"
    orientation="horizontal"
    description="The Dublin-Laurens County Chamber Community Foundation is led by a dedicated board of community members who are committed to the foundation's mission and vision."
  >
    <template #title>
      <h2
        class="text-3xl sm:text-4xl lg:text-5xl text-pretty tracking-tight font-bold text-highlighted text-center lg:text-left"
      >
        Board Members
      </h2>
    </template>
    <div class="grid grid-cols-2 sm:grid-cols-3 gap-6">
      <BoardMemberCard
        v-for="member in boardMembers"
        :key="member.name"
        :src="member.src"
        :name="member.name"
        :title="member.title"
      />
    </div>
  </UPageSection>
</template>
