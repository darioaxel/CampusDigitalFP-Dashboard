<template>
  <NuxtLoadingIndicator :color="false" class="z-100 bg-primary/80" />
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
  <Toaster />
  <LayoutFooter />
</template>

<script setup lang="ts">
import Toaster from '@/components/ui/toast/Toaster.vue';

</script>
