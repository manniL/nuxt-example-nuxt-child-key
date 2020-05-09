<template>
  <div>
    <div style="padding: 3rem">
      <NuxtLink to="nuxt">Nuxt</NuxtLink>
      <NuxtLink to="vue">Vue</NuxtLink>
    </div>

    <Transition name="fade">
      <div :key="'vue'" v-if="$route.path.endsWith('/nuxt')">
        <NuxtChild />
      </div>
      <div :key="'nuxt'" v-if="$route.path.endsWith('/vue')">
        <NuxtChild />
      </div>
    </Transition>
  </div>
</template>

<style>
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>
