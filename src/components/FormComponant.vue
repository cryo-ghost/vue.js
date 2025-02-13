<template>
    <form class="custom-form">
        <section class="custom-form_fields-section">
          <FieldComponent 
            v-for="(field, index) in data.fields" 
            :key="index"
            :data="field"
          />
        </section>
        <section class="custom-form_fields-section">
           <ButtonComponent 
              v-for="(button, index) in data.buttons"
              :key="index"
              :data="button"
           />
        </section>

      </form>
</template>
<script setup lang="ts">
import FieldComponent from './FieldComponent.vue'
import ButtonComponent from './ButtonComponent.vue';


  interface FormComponantProperties {
    data: {
        fields: Array<{id: string, type?: string, placeholder: string, class?: string}>,
        buttons: any
    }
  }

  defineProps<FormComponantProperties>()


</script>