<script setup lang="ts">
import RouterHeader from '@/components/layout/HeaderCont.vue'
import RouterFooter from '@/components/layout/FooterCont.vue'
</script>

<style lang="scss">
@use 'style.scss';
</style>

<template>
  <RouterHeader />
  <router-view />
  <RouterFooter />
</template>
