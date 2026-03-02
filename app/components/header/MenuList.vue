<template>
  <div @click="showMenu = !showMenu" class="sm:hidden">
    <div class="flex flex-col gap-2 cursor-pointer">
      <p class="w-10 border opacity-60"></p>
      <p class="w-10 border opacity-60"></p>
      <p class="w-10 border opacity-60"></p>
    </div>
    <nav
        v-if="showMenu"
        class="absolute">
      <ul :class="[base, variants.adaptive]">
        <li v-for="item in menu">
          <NuxtLink :to="item.link">
            {{ item.name }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
  </div>

  <nav class="absolute sm:flex hidden">
    <ul :class="[base, variants.row]">
      <li v-for="item in menu">
        <NuxtLink :to="item.link">
          {{ item.name }}
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script lang="ts" setup>

const {data: menu} = await useFetch('/api/menu')

const base = 'flex uppercase hover:font-bold '

const variants = {
  row: 'items-center justify-around gap-5',
  adaptive: 'flex-col gap-2 bg-card relative top-0 right-0 p-2 rounded-l rounded-b'
}

const showMenu = ref<boolean>(false)

</script>

<style scoped>

</style>
