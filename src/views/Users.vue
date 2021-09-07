<template>
  <div>
    <h1>Users</h1>
    <button @click="toHome">Homeへいく</button>
    <hr>
    <h1>User No. {{ id }}</h1>
    <router-link :to="{ name: 'user-id-profile', params: { id: Number(id) + 1}}">次のユーザー</router-link>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  props: ["id"],
  methods: {
    toHome() {
      this.$router.push('/')
    }
  }
}
</script>