<script setup lang="ts">
import AppNavi, { MenuItem } from "./components/AppNavi.vue";

const menuItems: MenuItem[] = [
    {
        type: "heading",
        title: "Main",
    },
    {
        type: "menu",
        title: "ToDo",
        icon: "fa-list",
        url: "/todo",
    },
];
</script>

<template>
    <router-view />
    <AppNavi title="Todo App" :menu-items="menuItems"></AppNavi>
</template>

<style scoped>
.logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
}
.logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
    filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
