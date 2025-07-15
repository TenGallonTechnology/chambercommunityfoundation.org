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
    name: 'Joey Barrett',
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
    src: '/board/guy-cochran.jpg',
    name: 'Guy Cochran',
    title: ''
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
    src: '/board/phil-patel.jpg',
    name: 'Phil Patel',
    title: ''
  },
  {
    src: '/board/heath-taylor.jpg',
    name: 'Heath Taylor',
    title: ''
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
    title="Board Members"
    description="The Dublin-Laurens County Chamber Community Foundation is led by a dedicated board of community members who are committed to the foundation's mission and vision."
  >
    <div class="grid grid-cols-2 sm:grid-cols-3 gap-6 ">
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
