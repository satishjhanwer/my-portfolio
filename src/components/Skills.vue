<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" :id="id">
    <div class="my-auto">
      <h2 class="mb-5">{{title}}</h2>
      <div class="subheading mb-3">{{subHeading1}}</div>
      <ul class="list-inline list-icons">
        <li class="list-inline-item" v-for="skill in skills" :key="skill.name">
          <i :class="'devicons '+ skill.icon +''" :title="''+ skill.level +''"></i>
        </li>
      </ul>
      <div class="subheading mb-3">{{subHeading2}}</div>
      <ul class="fa-ul mb-0">
        <li v-for="role in responsibility" :key="role.id">
          <i class="fa-li fa fa-check"></i>
          {{ role.text }}
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Skills',
  props: ['id', 'skills', 'responsibility'],
  data () {
    return {
      title: 'Skills',
      subHeading1: 'Programming Languages & Tools',
      subHeading2: 'Job Related Responsibility'
    }
  }
}
</script>
