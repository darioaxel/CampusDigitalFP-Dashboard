<script setup lang="ts">
import AppSidebar from '@/components/AppSidebar.vue'
import { SidebarProvider, SidebarTrigger } from '@/components/ui/sidebar'

definePageMeta({
  layout: 'board'
})
</script>

<template>
  <SidebarProvider>
    <AppSidebar />
    <main>
      <SidebarTrigger />
      Hola Sidebar!
    </main>
  </SidebarProvider>
</template>


