<script setup lang="ts">
import { number, object, string } from 'yup';
import { useForm } from 'vee-validate';

const schema = object({
  name: string().required().label('Name'),
  email: string().required().email().label('Email'),
  age: number().required().label('Age'),
});

const { handleSubmit, resetForm } = useForm({
  validationSchema: schema,
});

const onSubmit = handleSubmit((values) => {
  alert(JSON.stringify(values));
});
</script>

<template>
  <div class="mt-[5rem] mx-auto w-3/4">
    <VCard>
      <form @submit="onSubmit" class="border-none">
        <VInput wrapper-class="mb-2" name="name" label="Name" placeholder="Your Name" />
        <VInput wrapper-class="mb-2" name="email" label="Email" placeholder="Your Email" />
        <VInput wrapper-class="mb-2" name="age" label="Age" placeholder="Your Age" />
        <div class="mt-4">
          <VBtn type="submit" color="primary" class="mr-3">Submit</VBtn>
          <VBtn type="button" color="secondary" @click="resetForm">Reset</VBtn>
        </div>
      </form>
    </VCard>
  </div>
</template>
