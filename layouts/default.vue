<template>
    <a-layout>
        <a-layout-header class="layout" >
            <a-row align="middle" style="height: 100px;">
                <a-col span=12>
                    <a-flex vertical>
                        <span style="font-family: Hiraya; font-size: 20px; color: var(--primary-color); line-height: 15px;">salinx</span>
                        <h1 style="padding: 0px; margin: 0px; line-height: 45px; font-size: 50px; font-weight: 500;">Salin</h1>
                    </a-flex>
                </a-col>
                <a-col span=12>
                    <a-flex justify="flex-end" align="center">
                        <a-menu
                            mode="horizontal"
                            :style="{ 
                                lineHeight: '64px', 
                                border: 'none',
                                fontSize: '16px',
                                fontWeight: 300,
                                width: '395px',
                                backgroundColor: '#fff'
                            }"
                            :items="items"
                        >   
                        </a-menu>
                    </a-flex>
                </a-col>
            </a-row>
        </a-layout-header>
        <a-layout-content class="layout" style="padding-top: 50px;">
            <slot />
        </a-layout-content>
    </a-layout>    
</template>
<script setup lang="ts">
    import type { MenuProps } from 'ant-design-vue';
    import { ReadOutlined, FontSizeOutlined, BuildOutlined } from '@ant-design/icons-vue'
    const items = ref<MenuProps['items']>([
        {
            key: '1',
            icon: () => h(ReadOutlined, {fontSize: 32}),
            label: 'TUKLASIN',
            title: 'TUKLASIN',
        },
        {
            key: '2',
            icon: () => h(FontSizeOutlined),
            label: 'MAG-SALIN',
            title: 'MAG-SALIN',
        },
        {
            key: '3',
            icon: () => h(BuildOutlined),
            label: 'PAGSASANAY',
            title: 'PAGSASANAY',
        },
    ])
</script>
<style scoped>
    .layout {
        padding: 0 300px;
        background-color: #fff;
        border: none;
    }
</style>