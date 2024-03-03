<template>
    <a-card>
      <template #title>
        
      </template>
      <template #extra>
          <a-switch v-model:checked="state.isChecked">
            <template #checkedChildren>
              <span style="font-weight: 300;"><FontSizeOutlined /> Teksto</span>
            </template>
            <template #unCheckedChildren>
              <span style="font-weight: 300;">Salita <SoundOutlined /></span>
            </template>
          </a-switch>
        </template>
      hello
    </a-card>
</template>
<script setup lang="ts">
  definePageMeta({
    layout: 'default'
  })

  interface StateTypes {
    isChecked: boolean
  }

  const state = reactive<StateTypes>({
    isChecked: true
  })
</script>