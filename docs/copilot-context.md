# Documentation Links and Context

## Quick Reference Links

### NuxtUI Pro

- **Main Documentation**: <https://ui.nuxt.com/pro>
- **Components**: <https://ui.nuxt.com/pro/components>
- **Templates**: <https://ui.nuxt.com/pro/templates>
- **Examples**: <https://ui.nuxt.com/pro/examples>

### Nuxt 3

- **Main Documentation**: <https://nuxt.com/docs>
- **Getting Started**: <https://nuxt.com/docs/getting-started>
- **API Reference**: <https://nuxt.com/docs/api>
- **Examples**: <https://nuxt.com/docs/examples>

### Vue 3

- **Composition API**: <https://vuejs.org/guide/>
- **API Reference**: <https://vuejs.org/api/>
- **TypeScript with Vue**: <https://vuejs.org/guide/typescript/>

### TailwindCSS

- **Documentation**: <https://tailwindcss.com/docs>
- **Components**: <https://tailwindui.com/components>

### Iconify

- **Icon Sets**: <https://iconify.design/>
- **Lucide Icons**: <https://lucide.dev/icons/>
- **Simple Icons**: <https://simpleicons.org/>

## Common Patterns in This Project

### NuxtUI Component Patterns

```typescript
// Button variants
UButton: {
  color: "primary" |
    "gray" |
    "red" |
    "orange" |
    "amber" |
    "yellow" |
    "lime" |
    "green" |
    "emerald" |
    "teal" |
    "cyan" |
    "sky" |
    "blue" |
    "indigo" |
    "violet" |
    "purple" |
    "fuchsia" |
    "pink" |
    "rose";
  variant: "solid" | "outline" | "soft" | "ghost" | "link";
  size: "xs" | "sm" | "md" | "lg" | "xl";
}

// Card variants
UCard: {
  ui: {
    body: {
      padding: "p-4 sm:p-6";
    }
    header: {
      padding: "px-4 py-5 sm:px-6";
    }
  }
}

// Container responsive
UContainer: {
  size: "xs" |
    "sm" |
    "md" |
    "lg" |
    "xl" |
    "2xl" |
    "3xl" |
    "4xl" |
    "5xl" |
    "6xl" |
    "7xl";
}
```

### Nuxt 3 Composables

```typescript
// Navigation
navigateTo("/path");
navigateTo({ name: "route-name" });

// Data fetching
const { data } = await useFetch("/api/endpoint");
const { data } = await useLazyFetch("/api/endpoint");

// SEO
useSeoMeta({
  title: "Page Title",
  description: "Page description",
});

useHead({
  title: "Page Title",
});

// Page meta
definePageMeta({
  title: "Page Title",
  layout: "custom",
});
```

### TypeScript Interfaces

```typescript
// Board member interface (project specific)
interface BoardMember {
  name: string;
  position: string;
  image: string;
  bio?: string;
}

// Component props pattern
interface Props {
  title: string;
  description?: string;
  variant?: "default" | "featured";
}

// Event handlers
interface Events {
  click: (event: MouseEvent) => void;
  submit: (data: FormData) => void;
}
```

## File Structure Conventions

```
~/components/
  ├── ui/           # Reusable UI components
  ├── layout/       # Layout-specific components
  └── page/         # Page-specific components

~/pages/
  ├── index.vue     # Homepage
  ├── about.vue     # About page
  └── [...slug].vue # Dynamic routes

~/composables/
  ├── useApi.ts     # API utilities
  └── useAuth.ts    # Authentication

~/utils/
  ├── constants.ts  # App constants
  └── helpers.ts    # Helper functions
```

## Code Generation Guidelines

When generating components:

1. Always use TypeScript
2. Use Composition API with `<script setup>`
3. Include proper TypeScript interfaces
4. Use NuxtUI components when possible
5. Add SEO meta tags for pages
6. Include proper accessibility attributes
7. Use semantic HTML structure
8. Follow the project's naming conventions
