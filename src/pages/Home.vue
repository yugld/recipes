<script setup>
    import AppLayout from '@/layouts/AppLayout.vue';
    import AppButton from '@/components/AppButton.vue';
</script>

<template>
        <AppLayout >
            <template #title>Рецепты</template>
            <template #controls>
                <router-link :to="getRecipePath('new')">
                    <AppButton text="Добавить рецепт"></AppButton>
                </router-link>
            </template>
        </AppLayout>
</template>
