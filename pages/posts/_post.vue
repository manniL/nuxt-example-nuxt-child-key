<template>
  <div>
    <div>
      <NuxtLink to="nuxt">Nuxt</NuxtLink>
      <NuxtLink to="vue">Vue</NuxtLink>
    </div>

    <Transition appear name="fade">
      <div v-if="$route.path.endsWith('/nuxt')">
        <NuxtChild />
      </div>
      <div v-if="$route.path.endsWith('/vue')">
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
