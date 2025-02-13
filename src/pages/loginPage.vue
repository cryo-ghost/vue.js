<template>
    <FormComponant />
</template>
  
<script setup lang="ts">
    import { reactive, ref } from "vue"
    import FormComponant from "../components/FormComponant.vue"

    const formData = reactive({
        fields: [
            {
                id: "email",
            type: "email",
            placeholder: "email"
            },
            {
            id: "password",
            type: "password",
            placeholder: "password"
            }


        ],
        buttons: [
            {
                id: "submit-button",
                type: "set",
                testContent: "Valider",
                class: "is-primary"
            }

        ] as any
    })

</script>
  
<style lang="scss">

</style>
  