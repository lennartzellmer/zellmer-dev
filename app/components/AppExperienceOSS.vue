<script setup lang="ts">
const work = [
  {
    project: 'Vorfall',
    description: 'Type-safe event sourcing with MongoDB and projections',
    logo: 'ph:git-pull-request',
    link: 'https://github.com/lennartzellmer/vorfall',
  },
] as const
</script>

<template>
  <div>
    <div class="flex gap-2 items-center text-slate-12 font-semibold dark:text-slate-dark-12 text-base">
      <Icon
        name="ph:code-block"
        class="size-6 text-slate-10 dark:text-slate-dark-10"
      />
      Open Source Work
    </div>
    <div class="grid gap-6 mt-8">
      <NuxtLink
        v-for="(entry, index) in work"
        :key="index"
        :to="entry.link"
        class="flex gap-4 items-center group relative"
      >
        <div class="absolute -inset-3 bg-slate-3 dark:bg-slate-dark-3 rounded-lg opacity-0 group-hover:opacity-100 transition-opacity z-0" />
        <div class="z-10 bg-[#F0E8E5] size-10 text-slate-12 dark:text-slate-dark-12 shrink-0 grid place-items-center rounded-full ring-4 ring-white/70 dark:ring-slate-12 shadow-lg">
          <Icon name="ph:git-pull-request" />
        </div>
        <div class="z-10 grid w-full">
          <p class=" font-semibold text-slate-12 leading-tight dark:text-slate-dark-12">
            {{ entry.project }}
          </p>
          <span class="text-sm text-slate-10 dark:text-slate-dark-11">{{ entry.description }}</span>
        </div>
      </nuxtlink>
    </div>
  </div>
</template>
