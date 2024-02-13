<template>
  <section class="base-yes">
    <div class="base-yes__decor">
      <div class="base-yes__decor-left">
        <IconHearts :width="400" />
      </div>
      <div class="base-yes__decor-right">
        <IconHearts :width="400" />
      </div>
    </div>
    <div class="base-yes__body">
      <img class="base-yes__body-img" :src="yesImg" />
      <span class="base-yes__body-text">
        Я то абобус, а ты моя любимая валентинка ♥
      </span>
    </div>
  </section>
</template>

<script setup lang="ts">
import yesImg from "~/assets/yes.gif";
</script>

<style scoped lang="scss" src="./BaseYes.scss" />
