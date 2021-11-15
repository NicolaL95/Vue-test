<template>
  <div>
    <Test
      v-for="post in posts"
      v-bind:key="post.id"
      v-bind:title="post.title"
    ></Test>
  </div>
</template>

<script>
import Test from "./components/Test.vue";

Vue.component("app-user", {
  data: function () {
    return {
      users: [
        {
          username: "max",
        },
        {
          username: "max",
        },
        {
          username: "max",
        },
      ],
    };
  },
  template:
    '<div class="user" v-for="user in users"><p>username: {{user.username }} </p></div>',
});

export default {
  name: "App",
  components: {
    Test,
  },
  data() {
    return {
      posts: [
        { id: 1, title: "My journey with Vue" },
        { id: 2, title: "Blogging with Vue" },
        { id: 3, title: "Why Vue is so fun" },
      ],
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
