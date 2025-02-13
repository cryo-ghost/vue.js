<template>
    <button 
    :id="data.id"
    :type="data.type ? data.type : 'button'"
    :class="'button' + (data.class ? data.class : '')">
        {{ data.textContent }}
    </button>
</template>
<script setup lang="ts">

    interface ButtonComponantProperties {
        data: {
            id: string,
            textContent: string,
            class?: string,
            type: 'submit'| 'reset' |'button',
        }
    }

    defineProps<ButtonComponantProperties>()


</script>