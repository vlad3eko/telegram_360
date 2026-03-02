<template>
  <div class="flex items-center justify-between w-full">
    <div class="flex gap-5 items-center w-full max-md:justify-between">
      <div class="flex items-center">
        <Logo/>
        <h5>Telega360</h5>
      </div>
      <MenuList/>
    </div>
    <div class="flex gap-5">
      <Inputs type="search"/>
      <Button variant="primary">Подключить</Button>
    </div>
  </div>
</template>
<script setup lang="ts">
import Logo from "~/components/header/Logo.vue";
import Inputs from "~/components/UI/inputs/Inputs.vue";
import Button from "~/components/UI/button/Button.vue";
import MenuList from "~/components/header/MenuList.vue";
</script>
