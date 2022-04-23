<template>
  <login-view v-if="!showChatView" @login="getUsername" />
  <chat-view v-if="showChatView" :username="username" />
</template>

<script>
import LoginView from "./components/LoginView.vue";
import ChatView from "./components/ChatView.vue";

export default {
  name: "App",
  components: {
    LoginView,
    ChatView,
  },
  data() {
    return {
      showChatView: false,
      username: "",
    };
  },
  methods: {
    getUsername(username) {
      this.username = username;
      this.showChatView = true;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
