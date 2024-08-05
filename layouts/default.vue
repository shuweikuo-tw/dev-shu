<script lang="ts">
import AppHeader from '~/components/App/AppHeader.vue';
import AppFooter from '~/components/App/AppFooter.vue';


</script>
<template>
  <AppHeader />
  <div>
    <slot />
  </div>
  <AppFooter />
</template>
