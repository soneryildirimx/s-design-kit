<script setup>
import { ElButton } from 'element-plus'

const props = defineProps({
    text: {
        type: String,
        require: true
    },
    type: {
        type: String,
    },
    size: {
        type: String,
    },
    disabled: {
        type: Boolean,
    },
    block: {
        type: Boolean
    },
    icon: {
        type: String
    },

    iconRight: {
        type: Boolean
    }

})
</script>

<template>
    <el-button :text="false" :type="type" :size="size" :disabled="disabled" :icon="icon"
        :class="{ 'is-block': block, 'icon-right': iconRight }">
        {{ text }}
    </el-button>
</template>

<style lang="scss" scoped>
// yarn add @element-plus/icons-vue
.el-button {

    width: 93px;
    height: 40px;
    border-radius: 10px;

    &--small {
        width: 70px;
        height: 30px;
    }

    &--large {
        width: 110px;
        height: 50px;
    }

    &.is-disabled {
        background-color: $disabled;
        border-color: $disabled;
    }

    &.is-block {
        display: block;
        width: 100%;
    }

    &.icon-right {
        :deep() {
            .el-icon {
                order: 1;
            }

            >span {
                margin-left: 0;
                margin-right: 6px;
            }
        }
    }


    &.is-loading {
        :deep() {
            >span {
                display: none !important;
            }
        }
    }


}
</style>    