<template>
  <a-config-provider
    :theme="{
      token: useTheme(),
    }"
  >
    <NuxtLayout>
      <NuxtPage/>
    </NuxtLayout>
  </a-config-provider>
</template>

<script lang="ts">

</script>