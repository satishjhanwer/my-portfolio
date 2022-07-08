<script setup>
defineProps({
  id: {
    type: String,
    required: true,
  },
  social: {
    type: Array,
    required: true,
  },
  user: {
    type: Object,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <section class="resume-section p-3 p-lg-5 d-flex d-column" :id="id">
    <div class="my-auto">
      <div class="subheading">Hi there! I'm</div>
      <h1 class="mb-0">
        {{ user.name }}
        <span class="text-primary">{{ user.surname }}</span>
      </h1>
      <div class="subheading mb-5">
        {{ user.address }}
        <a :href="'mailto:' + user.email">{{ user.email }}</a>
      </div>
      <p class="mb-5">{{ user.introduction }}</p>
      <ul class="list-inline list-social-icons mb-0">
        <li class="list-inline-item" v-for="soc in social" :key="soc.name">
          <a
            :href="'' + soc.url + ''"
            target="_blank"
            rel="noreferrer"
            :aria-label="'' + soc.name + ''"
          >
            <span class="fa-stack fa-lg" :title="'' + soc.name + ''">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i
                :class="'fa ' + soc.icon + ' fa-stack-1x fa-inverse'"
                :title="'' + soc.name + ''"
              ></i>
            </span>
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>
