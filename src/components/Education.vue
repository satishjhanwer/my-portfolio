<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" :id="id">
    <div class="my-auto">
      <h2 class="mb-5">{{title}}</h2>
      <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="edu in education" :key="edu.degree">
        <div class="resume-content mr-auto">
          <h3 class="mb-0">{{ edu.name }}</h3>
          <div class="subheading mb-3">{{ edu.degree }}</div>
          <div>{{ edu.stream }}</div>
          <p>{{ edu.marks }}</p>
        </div>
        <div class="resume-date text-md-right">
          <span class="text-primary">{{ edu.startDate }} - {{ edu.endDate }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Education',
  props: ['id', 'education'],
  data () {
    return {
      title: 'Education'
    }
  }
}
</script>
