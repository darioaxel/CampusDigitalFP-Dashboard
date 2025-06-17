<script setup lang="ts">
import { LucideCalendar, LucideHome, LucideInbox, LucideSearch, LucideSettings } from "#components";
import {
  Sidebar,
  SidebarContent,
  SidebarGroup,
  SidebarGroupContent,
  SidebarGroupLabel,
  SidebarMenu,
  SidebarMenuButton,
  SidebarMenuItem,
} from "@/components/ui/sidebar";

// Menu items.
const items = [
  {
    title: "Home",
    url: "#",
    icon: LucideHome,
  },
  {
    title: "Inbox",
    url: "#",
    icon: LucideInbox,
  },
  {
    title: "Calendar",
    url: "#",
    icon: LucideCalendar,
  },
  {
    title: "Search",
    url: "#",
    icon: LucideSearch,
  },
  {
    title: "Settings",
    url: "#",
    icon: LucideSettings,
  },
];

</script>

<template>
  <Sidebar>
    <SidebarContent>
      <SidebarGroup>
        <SidebarGroupLabel>Application</SidebarGroupLabel>
        <SidebarGroupContent>
          <SidebarMenu>
              <SidebarMenuItem v-for="item in items" :key="item.title">
                <SidebarMenuButton asChild>
                    <a :href="item.url">
                      <component :is="item.icon" />
                      <span>{{item.title}}</span>
                    </a>
                </SidebarMenuButton>
              </SidebarMenuItem>
          </SidebarMenu>
        </SidebarGroupContent>
      </SidebarGroup>
    </SidebarContent>
  </Sidebar>
</template>