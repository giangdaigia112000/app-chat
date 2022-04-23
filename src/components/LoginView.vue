<template>
  <div>
    <input type="text" v-model="username" />
    <button @click="Login">Đăng nhập</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      username: "",
    };
  },
  methods: {
    Login() {
      this.$emit("login", this.username);
    },
  },
};
</script>
