<template>
  <!-- <header>
    <nav>
      <ul>
        <li class="nav-item">
            <img src="./assets/build-a-bot-logo.png" alt="logo">
            Build-a-Bot
        </li>
        <li>
          User: {{ user.userName }}
          <button @click="changeUserName()">Change</button>
        </li>
      </ul>
    </nav>
  </header> -->
  <main>
    <RobotBuilder />
  </main>
</template>

<script>
// import HomePage from './home/HomePage.vue';
import RobotBuilder from './build/RobotBuilder.vue';
// import Search from './search/Search.vue';

export default {
  name: 'App',
  components: {
    RobotBuilder,
    // Search,
  },
  // data() {
  //   return {
  //     user: { userName: 'Kristoffer' },
  //   };
  // },
  provide() {
    return { user: this.user };
  },
  // methods: {
  //   changeUserName() {
  //     this.user.userName = 'Stigh';
  //   },
  // },
};
</script>

<style>
body {
  background: linear-gradient(to bottom, #555, #999);
  background-attachment: fixed;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
.nav-item {
  height: 100px;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-content: center;
  text-align: center;
}
main {
  margin: 0 auto;
  padding: 30px;
  background-color: white;
  width: 1024px;
  min-height: 300px;
}
</style>
