<template>
  <div @mouseenter="showMenu = true" @mouseleave="showMenu = false" class="md:hidden max-md:mr-10">
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
          <NuxtLink :to="item.link" :class="hover">
            {{ item.name }}
          </NuxtLink>
        </li>
        <Inputs type="search"/>
        <Button variant="primary">Подключить</Button>
      </ul>
    </nav>
  </div>

  <nav class="md:flex hidden mx-5">
    <ul :class="[base, variants.row]">
      <li v-for="item in menu">
        <NuxtLink :to="item.link" :class="hover">
          {{ item.name }}
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script lang="ts" setup>

import Button from "~/components/UI/button/Button.vue";
import Inputs from "~/components/UI/inputs/Inputs.vue";

const {data: menu} = await useFetch('/api/menu')

const base = 'flex uppercase text-accent-foreground/70'
const hover = 'hover:text-primary  hover:border-b text-xl'

const variants = {
  row: 'items-center justify-around gap-5',
  adaptive: 'flex-col gap-2 bg-card relative top-0 right-0 p-2 rounded-l rounded-b'
}

const showMenu = ref<boolean>(false)

</script>

<style scoped>

</style>
