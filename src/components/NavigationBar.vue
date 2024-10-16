<script setup lang="ts">
import image from "../assets/profile.jpg";
defineProps<{
  id: string;
  landingLink: string;
  navItems: Array<{
    title: string;
    link: string;
  }>;
}>();
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" :id="id">
    <a class="navbar-brand js-scroll-trigger" :href="landingLink">
      <span class="d-block d-lg-none">My Portfolio</span>
      <span class="d-none d-lg-block">
        <img class="img-fluid img-profile rounded-circle mx-auto mb-2" :src="image" alt="photo" />
      </span>
    </a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarItems"
      aria-controls="navbarItems"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarItems">
      <ul class="navbar-nav">
        <li class="nav-item" v-for="navItem in navItems" :key="navItem.title">
          <a class="nav-link js-scroll-trigger" :href="navItem.link">{{ navItem.title }}</a>
        </li>
      </ul>
    </div>
  </nav>
</template>
