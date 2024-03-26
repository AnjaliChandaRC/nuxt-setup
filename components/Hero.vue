<script setup>
const list = [
  {
    title: "text One",
    link: "/",
    para: "dfghjkl",
  },
  {
    title: "text Two",
    link: null,
    para: "dfghjkl",
  },
  {
    title: "text Three",
    link: "/two",
    para: "dfghjkl",
  },
];
</script>

<template>
  <div v-for="(obj, index) in list" :key="index">
    <NuxtLink :to="obj.link" v-if="obj.link">{{ obj.title }} </NuxtLink>
    <p v-else>{{ obj.title }}</p>
    <p class="text-red-800" :class="$route.path !== '/' && 'text-green-800'">
      {{ obj.para }}
    </p>
  </div>
</template>

<style scoped>
h2 {
  font-size: 100px;
}
</style>
