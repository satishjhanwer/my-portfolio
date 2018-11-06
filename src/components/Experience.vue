<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" :id="id">
    <div class="my-auto">
      <h2 class="mb-5">{{title}}</h2>
      <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="job in experience" :key="job.position">
        <div class="resume-content mr-auto">
          <h3 class="mb-0">{{ job.position }}</h3>
          <div class="subheading mb-3">{{ job.company }}</div>
          <p>{{ job.description }}</p>
        </div>
        <div class="resume-date text-md-right">
          <span class="text-primary">{{ job.startDate }} - {{ job.endDate }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Experience',
  props: ['id', 'experience'],
  data () {
    return {
      title: 'Experience'
    }
  }
}
</script>
