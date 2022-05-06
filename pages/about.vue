<template>
  <PageWrapper class="flex flex-col justify-center items-center">
    <PageHeader>
      <PageTitle :text="$t('pages.about.title')" class="capitalize" />
    </PageHeader>
    <PageBody>
      <div class="flex flex-col items-center">
        <img
          src="https://avatars.githubusercontent.com/u/41994283?v=4"
          class="inline-block rounded-full"
          alt="viandwi24"
          width="100"
          height="100"
        />
        <Button
          size="xs"
          text="Phạm Đức Nhật (@nhatpham0709)"
          class="font-extrabold mt-4"
          href="https://github.com/nhatpham0709"
        />
      </div>
    </PageBody>
  </PageWrapper>
</template>

<script lang="ts" setup>
definePageMeta({
  layout: 'page',
})
</script>
