<script setup>
defineProps({
  id: {
    type: String,
    required: true,
  },
  interest: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" :id="id">
    <div class="my-auto">
      <h2 class="mb-5">Interests</h2>
      <p class="mb-0">{{ interest }}</p>
    </div>
  </section>
</template>
