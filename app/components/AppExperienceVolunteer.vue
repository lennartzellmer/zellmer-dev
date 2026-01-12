<script setup lang="ts">
const voluneerWork = [
  {
    position: 'Systems Administrator',
    company: 'KIDS e.V.',
    timeframe: '2024 - Present',
    logoUrl: '/company_logos/kids.jpg',
    link: 'https://www.kids-bonn.de/',
  },
  {
    position: 'Fullstack Developer',
    company: 'Music&Al e.V.',
    timeframe: '2023 - Present',
    logoUrl: '/company_logos/musical.jpg',
    link: 'https://github.com/lennartzellmer/rbag-admin-panel',
  },
] as const
</script>

<template>
  <div>
    <div class="flex gap-2 items-center text-slate-12 font-semibold dark:text-slate-dark-12 text-base">
      <Icon
        name="ph:hand-heart"
        class="size-6 text-slate-10 dark:text-slate-dark-10"
      />
      Volunteer work
    </div>
    <div class="grid gap-6 mt-8">
      <NuxtLink
        v-for="(entry, index) in voluneerWork"
        :key="index"
        :to="entry.link"
        class="flex gap-4 items-center group relative"
      >
        <div class="absolute -inset-3 bg-slate-3 dark:bg-slate-dark-3 rounded-lg opacity-0 group-hover:opacity-100 transition-opacity z-0" />
        <NuxtImg
          :src="entry.logoUrl"
          alt="Company Logo"
          class="z-10 mt-2 size-10 w-auto object-cover rounded-full ring-4 ring-white/70 dark:ring-slate-12 shadow-lg"
          width="150"
          height="150"
        />
        <div class="z-10 grid w-full">
          <p class=" font-semibold text-slate-12 leading-tight dark:text-slate-dark-12">
            {{ entry.position }}
          </p>
          <span class="text-sm text-slate-10 dark:text-slate-dark-11">{{ entry.company }}</span>
        </div>
        <span class="z-10 text-sm whitespace-nowrap text-slate-11 dark:text-slate-dark-11">{{ entry.timeframe }}</span>
      </NuxtLink>
    </div>
  </div>
</template>
