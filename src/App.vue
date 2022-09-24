<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <div class="flex flex-col gap-10 items-center p-10">
    <header class="flex items-center gap-10">
      <img
        alt="Vue logo"
        class="logo"
        src="@/assets/logo.svg"
        width="125"
        height="125"
      />

      <strong class="text-3xl">+</strong>

      <img
        alt="Vue logo"
        class="logo"
        src="@/assets/electron.svg"
        width="125"
        height="125"
      />

      <strong class="text-3xl">+</strong>

      <img
        alt="Vue logo"
        class="logo"
        src="@/assets/vite.svg"
        width="125"
        height="125"
      />
    </header>

    <div class="flex flex-col items-center gap-10">
      <h1 class="text-5xl font-medium">Vue + Electron + Vite + TypeScript</h1>
      <nav
        class="flex gap-1 w-64 h-10 bg-[#191919] border border-[#2a2a2a] p-1 rounded-lg shadow-inner text-lg"
      >
        <RouterLink
          class="w-full flex items-center justify-center gap-2"
          to="/"
        >
          Home
        </RouterLink>
        <RouterLink
          class="w-full flex items-center justify-center gap-2"
          to="/about"
        >
          About
        </RouterLink>
      </nav>
    </div>
  </div>

  <main class="mt-20 text-center flex flex-col gap-4 text-lg">
    <RouterView />
  </main>
</template>

<style lang="postcss">
body {
  @apply overflow-hidden;
}

#app {
  @apply m-0 p-0 w-screen h-screen bg-[#1c1c1c] text-white overflow-auto;
}

.router-link-active {
  @apply bg-[#242424] shadow  rounded-lg;
}

::-webkit-scrollbar {
  width: 6px;
}

::-webkit-scrollbar:hover {
  width: 12px;
}

::-webkit-scrollbar-track {
  background-color: transparent;
}

::-webkit-scrollbar-thumb {
  @apply rounded shadow bg-slate-200/50;
}
</style>
