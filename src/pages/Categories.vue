<script setup>
    import {ref, onMounted, computed } from 'vue';
    import { useRootStore } from '@/stores/root';
    import AppLayout from '@/layouts/AppLayout.vue';
    import AppButton from '@/components/AppButton.vue';

    const rootStore = useRootStore();
    const categories = computed(() => rootStore.categories);
</script>
    
<template>
    <AppLayout>
        <template #title>Категории</template>
        <template #inner>
        <el-table :data="categories" style="width: 100%">
            <el-table-column prop="strCategory" label="Category" />
        </el-table>  
        </template>
    </AppLayout>
</template>
