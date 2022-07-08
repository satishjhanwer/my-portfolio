<script setup>
defineProps({
  id: {
    type: String,
    required: true,
  },
  accomplishment: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" :id="id">
    <div class="my-auto">
      <h2 class="mb-5">Awards & Certifications</h2>
      <ul class="fa-ul mb-0">
        <li v-for="acc in accomplishment" :key="acc.id">
          <i class="fa-li fa fa-trophy text-warning"></i>
          {{ acc.text }} - {{ acc.company }} - {{ acc.date }}
        </li>
      </ul>
    </div>
  </section>
</template>
