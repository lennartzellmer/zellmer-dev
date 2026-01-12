<script setup lang="ts">
useHead({
  title: 'Hi, Lennart here!',
  meta: [
    {
      name: 'description',
      content: 'Sharing thoughts and concepts around Product, Design and Development.',
    },
  ],
})

defineOgImageComponent('DefaultPage', {
  title: 'Hi, Lennart here!',
  description: 'Sharing thoughts and concepts around Product, Design and Development.',
})
</script>

<template>
  <main>
    <HomeHeader />
    <section class="mx-auto mt-4 max-w-7xl px-4 sm:mt-8 md:mt-28 grid gap-8 grid-cols-12">
      <LatestBlogPosts class="col-span-12 sm:col-span-7" />
      <div class="border-l border-slate-3 dark:border-slate-dark-2 col-span-12 sm:col-span-4 self-start p-8 my-8 gap-16 grid">
        <AppExperienceWork />
        <AppExperienceOSS />
        <AppExperienceVolunteer />
      </div>
    </section>
  </main>
</template>
