# GitHub Copilot Instructions for Chamber Community Foundation

## Project Overview
This is a Nuxt 3 application built with NuxtUI Pro for the Chamber Community Foundation website. The project uses TypeScript, TailwindCSS, and follows Nuxt 3 best practices.

## Tech Stack
- **Framework**: Nuxt 3.17+ (with compatibility version 4)
- **UI Library**: NuxtUI Pro 3.1+ (built on TailwindCSS and Headless UI)
- **Styling**: TailwindCSS (configured through NuxtUI)
- **Icons**: Iconify (Lucide and Simple Icons collections)
- **Language**: TypeScript
- **Package Manager**: pnpm

## Code Style & Conventions

### Vue/Nuxt Patterns
- Use Composition API with `<script setup>`
- Prefer `definePageMeta()` for page-level configuration
- Use `navigateTo()` for programmatic navigation
- Leverage Nuxt auto-imports (no need to import composables)
- Use `useLazyFetch()` and `useFetch()` for data fetching
- Implement proper SEO with `useSeoMeta()` and `useHead()`

### NuxtUI Component Usage
- Always use NuxtUI Pro components when available (UButton, UCard, UInput, etc.)
- Follow NuxtUI Pro naming conventions (prefix with 'U')
- Use NuxtUI Pro's built-in props for styling (color, variant, size)
- Leverage NuxtUI Pro's responsive utilities
- Use NuxtUI Pro icons through the `icon` prop

### Component Structure
```vue
<template>
  <!-- Use semantic HTML with NuxtUI components -->
  <UContainer>
    <UCard>
      <template #header>
        <h2>{{ title }}</h2>
      </template>
      <!-- Content -->
    </UCard>
  </UContainer>
</template>

<script setup lang="ts">
// TypeScript interfaces
interface Props {
  title: string
}

// Component props
defineProps<Props>()

// SEO meta
useSeoMeta({
  title: () => title
})
</script>
```

### File Organization
- Components: `~/components/` (auto-imported)
- Pages: `~/pages/` (file-based routing)
- Composables: `~/composables/` (auto-imported)
- Utils: `~/utils/` (auto-imported)
- Assets: `~/assets/` for processed assets
- Public: `~/public/` for static files

## NuxtUI Pro Component Guidelines

### Common Components to Use
- `UButton` - for all buttons with proper variants
- `UCard` - for content containers
- `UContainer` - for page-level containers
- `UInput`, `UTextarea`, `USelect` - for forms
- `UModal`, `USlideOver` - for overlays
- `UBadge` - for status indicators
- `UAvatar` - for user images
- `UIcon` - for icons (uses Iconify)

### Styling Approach
- Use NuxtUI Pro's built-in color system
- Leverage TailwindCSS utilities sparingly (NuxtUI props preferred)
- Use NuxtUI Pro's spacing and layout utilities
- Implement responsive design with NuxtUI Pro's responsive props

### Accessibility
- Always include proper ARIA labels
- Use semantic HTML elements
- Ensure keyboard navigation works
- Test with screen readers in mind
- Use NuxtUI Pro's built-in accessibility features

## Specific Project Context
- This is a community foundation website
- Focus on clean, professional design
- Ensure mobile responsiveness
- Include proper SEO meta tags
- Use board member data from the existing structure

## Documentation References
When suggesting code, refer to:
- NuxtUI Pro Documentation: https://ui.nuxt.com/pro
- Nuxt 3 Documentation: https://nuxt.com/docs
- Vue 3 Composition API: https://vuejs.org/guide/
- TailwindCSS: https://tailwindcss.com/docs
- Iconify: https://iconify.design/

## Example Patterns

### Page Component
```vue
<template>
  <UContainer>
    <UPageHeader 
      :title="page.title" 
      :description="page.description" 
    />
    <UPageBody>
      <!-- Page content -->
    </UPageBody>
  </UContainer>
</template>

<script setup lang="ts">
definePageMeta({
  title: 'Page Title'
})

const page = {
  title: 'Chamber Community Foundation',
  description: 'Supporting our community through strategic giving'
}

useSeoMeta({
  title: page.title,
  description: page.description
})
</script>
```

### Component with Props
```vue
<template>
  <UCard>
    <div class="flex items-center gap-4">
      <UAvatar :src="member.image" :alt="member.name" size="lg" />
      <div>
        <h3 class="font-semibold">{{ member.name }}</h3>
        <p class="text-gray-500">{{ member.position }}</p>
      </div>
    </div>
  </UCard>
</template>

<script setup lang="ts">
interface BoardMember {
  name: string
  position: string
  image: string
}

interface Props {
  member: BoardMember
}

defineProps<Props>()
</script>
```

## Important Notes
- Always use TypeScript types and interfaces
- Prefer NuxtUI Pro components over custom styled components
- Use auto-imports provided by Nuxt (no need to import composables)
- Follow the existing project structure and naming conventions
- Ensure all suggestions are compatible with Nuxt 3.17+ and NuxtUI Pro 3.1+