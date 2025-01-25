<template>
  <div class="flex h-full w-72 flex-none flex-col bg-[#28343d] text-[#ddd]">
    <TagSrcTabSelf v-show="tagStore.tagSrc === 'star'" />
  </div>
</template>

<script setup>
import TagSrcTabSelf from './tag-src-self/index.vue';
import { useUserStore } from '@/store/user';
import { useTagStore } from '@/store/tag';
import { BRAND, BRAND_URI } from '@/constants';

const userStore = useUserStore();
const tagStore = useTagStore();
</script>

<style scoped>
:deep(.tag-item) {
  border-left: 0.25rem solid transparent;
}

:deep(.tag-item.selected) {
  border-left-color: var(--primary);
  background-color: #ffffff22;
}
</style>
