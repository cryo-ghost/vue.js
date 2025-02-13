<template>
    <article>
        <label v-bind:for="data.id"></label>
        <input 
        v-bind:type="data.type ? data.type : 'text'"
        v-bind:placeholder="data.placeholder"
        v-bind:class="'input' + data.class ? data.class : ''"
        />
    </article>
</template>
<script setup lang="ts">

    interface FieldComponantProperties {
        data: {
            id: string,
            type?: string,
            placeholder:string,
            class?:string,
        }
    }

    defineProps<FieldComponantProperties>()


</script>