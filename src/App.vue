<script setup lang="ts">
import { NConfigProvider } from 'naive-ui'
import { NaiveProvider } from '@/components/common'
import { useTheme } from '@/hooks/useTheme'
import { useLanguage } from '@/hooks/useLanguage'

const { theme, themeOverrides } = useTheme()
const { language } = useLanguage()
</script>

<template>
 
  <NConfigProvider
    class="h-full"
    :theme="theme"
    :theme-overrides="themeOverrides"
    :locale="language"
  > <img src="https://cdn.staticaly.com/gh/845415120/picx-images-hosting@master/20230714/微信图片_20230714092811.5jyfa9m4gso0.webp" alt="江鹏利-面试" style="width:400px;">
    <NaiveProvider>
      <RouterView />
    </NaiveProvider>
  </NConfigProvider>
  
</template>
