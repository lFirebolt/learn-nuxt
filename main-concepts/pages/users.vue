<template>
  <div>
    <h1>Users Page</h1>
    <div>
      <input type="text" v-model="userId" />
      <button @click="onLoadUser">Load User</button>
    </div>
    <nuxt-child />
  </div>
</template>

<script>
export default {
  data() {
    return {
      userId: ""
    };
  },

  methods: {
    onLoadUser() {
      this.$router.push("/users/" + this.userId);
    }
  },

  layout: "users"
};
</script>

<style scoped></style>
