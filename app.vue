<template>
  <div>
    <h1>Hello Nuxt3</h1>
    <p>by hidetaro7</p>

    <h2>Server API test</h2>
    <ul>
      <li v-for="user in users">{{ user.name }} さんは {{ user.old }} 歳</li>
    </ul>
  </div>
</template>

<script setup>
const { data: users } = await useFetch("/api/users");
</script>
