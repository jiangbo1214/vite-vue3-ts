<template>
  <div>名字：{{ mainStore.name }}，长度：{{ mainStore.nameLength }}</div>
  <button @click="updateName">修改store中的name</button>
  <n-button>naive-ui</n-button>
</template>
<script setup lang="ts">
import { useMainStore } from '@/store/index'
import { NButton } from 'naive-ui'
const mainStore = useMainStore()

function updateName(): void {
  // mainStore.$patch({
  //   name: '名字被修改了，nameLength也会改变',
  // })
  mainStore.insertPost('123')
}
</script>
