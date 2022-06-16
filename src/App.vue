<script setup>
import Button from '@/components/Atoms/Button.vue'
import { Share } from '@element-plus/icons-vue'
</script>
<template>
    <div style="padding: 10px">
        <Button text="Test" type="primary" :icon="Share" iconRight />
    </div>
</template>

<style lang="scss">
@import "@/assets/style/main.scss";
</style>
