<script setup lang="ts">
defineProps<{
  id: string;
  skills: Array<{
    name: string;
    icon: string;
    level: string;
  }>;
  responsibility: Array<{
    id: number;
    text: string;
  }>;
}>();
</script>

<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" :id="id">
    <div class="my-auto">
      <h2 class="mb-5">Skills</h2>
      <div class="subheading mb-3">Programming Languages & Tools</div>
      <ul class="list-inline list-icons">
        <li class="list-inline-item" v-for="skill in skills" :key="skill.name">
          <i :class="skill.icon + ' colored'" :title="'' + skill.level + ''"></i>
        </li>
      </ul>
      <div class="subheading mb-3">Job Related Responsibility</div>
      <ul class="fa-ul mb-0">
        <li v-for="role in responsibility" :key="role.id">
          <i class="fa-li fa fa-check"></i>
          {{ role.text }}
        </li>
      </ul>
    </div>
  </section>
</template>
