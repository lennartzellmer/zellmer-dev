<script setup lang="ts">
const cvEntries = [
  {
    position: 'Senior Product Manager',
    company: 'elvah',
    logoUrl: '/company_logos/elvah.jpg',
    timeframe: '2025 - present',
  },
  {
    position: 'Developer / Senior Product Owner',
    company: 'elvah',
    logoUrl: '/company_logos/elvah.jpg',
    timeframe: '2020 - 25',
  },
  {
    position: 'Developer / Product Owner',
    company: 'kreait',
    timeframe: '2016 - 19',
    logoUrl: '/company_logos/kreait.jpg',
  },
] as const
</script>

<template>
  <div>
    <div class="flex gap-2 items-center text-slate-12 font-semibold dark:text-slate-dark-12 text-base">
      <Icon
        name="ph:toolbox"
        class="size-6 text-slate-10 dark:text-slate-dark-10"
      />
      Work
    </div>
    <div class="grid gap-6 mt-8">
      <div
        v-for="(entry, index) in cvEntries"
        :key="index"
        class="flex gap-4 items-center"
      >
        <NuxtImg
          :src="entry.logoUrl"
          alt="Company Logo"
          class="mt-2 size-10 w-auto object-cover rounded-full ring-4 ring-white/70 dark:ring-slate-12 shadow-lg"
          width="150"
          height="150"
        />
        <div class="grid w-full">
          <p class=" font-semibold text-slate-12 leading-tight dark:text-slate-dark-12">
            {{ entry.position }}
          </p>
          <span class="text-sm text-slate-10 dark:text-slate-dark-11">{{ entry.company }}</span>
        </div>
        <span class="text-sm whitespace-nowrap text-slate-11 dark:text-slate-dark-11">{{ entry.timeframe }}</span>
      </div>
    </div>
  </div>
</template>
