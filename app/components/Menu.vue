<template>
  <div class="flex items-center justify-between w-full">
    <div class="flex gap-5 items-center w-full max-md:justify-between">
      <div class="flex items-center gap-2">
        <Logo/>
        <div class="font-bold max-sm:hidden">
          <span class="text-primary/80 text-5xl">TG<Counter count="360" class="text-5xl"/></span>
        </div>
      </div>
      <MenuList/>
    </div>
    <div class="flex gap-5">
      <Inputs type="search" disabled/>
      <Button variant="primary">Подключить</Button>
    </div>
  </div>
</template>
<script setup lang="ts">
import Logo from "~/components/header/Logo.vue";
import Inputs from "~/components/UI/inputs/Inputs.vue";
import Button from "~/components/UI/button/Button.vue";
import MenuList from "~/components/header/MenuList.vue";
import Counter from "~/components/UI/Counter.vue";
</script>
