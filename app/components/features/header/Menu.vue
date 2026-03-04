<template>
  <header class="bg-background">
    <section class="bg-background container mx-auto  flex items-center justify-between w-full p-2 rounded-2xl ">
      <div class=" flex gap-5 items-center w-full max-md:justify-between">
        <Logo/>
        <MenuList/>
      </div>
      <div class="flex gap-5">
        <Inputs type="search" disabled/>
        <Button variant="primary">Подключить</Button>
      </div>
    </section>
  </header>
</template>
<script setup lang="ts">
import Logo from "~/components/features/header/Logo.vue";
import Inputs from "~/components/UI/inputs/Inputs.vue";
import Button from "~/components/UI/button/Button.vue";
import MenuList from "~/components/features/header/MenuList.vue";
</script>
