<template>
  <div>
    <h1>Hello Nuxt3</h1>
    <p>by hidetaro7</p>

    <h2>Server API test</h2>
    <ul>
      <li v-for="user in users">{{ user.name }} さんは {{ user.old }} 歳</li>
    </ul>

    <p>error: {{ error }}</p>
  </div>
</template>

<script setup>
const { data: users, error: error } = await useFetch("/api/users");
</script>
