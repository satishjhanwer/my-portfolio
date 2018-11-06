<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" :id="id">
    <div class="my-auto">
      <h2 class="mb-5">{{title}}</h2>
      <p class="mb-0"> {{ interest }}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Interests',
  props: ['id', 'interest'],
  data () {
    return {
      title: 'Interests'
    }
  }
}
</script>
