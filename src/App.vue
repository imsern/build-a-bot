<template>
  <header>
    <nav>
      <div class="nav-item">
        <router-link class="nav-link" :to="{ name: 'Home' }" exact>
          <img src="./assets/build-a-bot-logo.png" class="logo" />
          Build-a-Bot
        </router-link>
      </div>
      <div class="nav-item">
        <router-link class="nav-link" :to="{ name: 'Build' }" exact>
          Build
        </router-link>
      </div>
      <div class="nav-item cart">
        <router-link class="nav-link" :to="{ name: 'Cart' }" exact>
          Cart
        </router-link>
        <div class="cart-items">
          {{ cart.length }}
        </div>
      </div>
      <!-- <li>
          User: {{ user.userName }}
          <button @click="changeUserName()">Change</button>
        </li> -->
    </nav>
  </header>
  <div class="container">
    <aside class="aside">
      <router-view name="sidebar" />
    </aside>
    <main>
      <router-view />
      <!-- <RobotBuilder /> -->
    </main>
  </div>
</template>

<script>
// import HomePage from './home/HomePage.vue';
// import RobotBuilder from './build/RobotBuilder.vue';
// import Search from './search/Search.vue';

export default {
  name: 'App',
  computed: {
    cart() {
      return this.$store.state.cart;
    },
  },
  components: {
    // RobotBuilder,
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
main {
  padding: 30px;
  background-color: white;
  width: 964px;
  min-height: 300px;
}
header {
  width: 1184px;
  background: #999;
  margin: 0 auto;
}
.nav-item {
  display: inline-block;
  padding: 5px 10px;
  font-size: 22px;
  border-right: 1px solid rgba(190, 190, 190, 0.5);
}
.nav-item.cart{
  position: relative;
  margin-left: auto;
  border-right: none;
}
.logo {
  vertical-align: middle;
  height: 50px;
}
.nav-link {
  text-decoration: none;
  color: inherit;
}
.router-link-active {
  color: white;
}
.container {
  display: flex;
  margin: 10px auto 0 auto;
  justify-content: center;
}
.aside {
  padding: 30px;
  background-color: #aaa;
  width: 100px;
  min-height: 300px;
}
.cart-items{
  position: absolute;
  top: -5px;
  right: -9px;
  font-size: 18px;
  width: 20px;
  text-align: center;
  display: inline-block;
  border-radius: 100px;
  background-color: mediumseagreen;
}
</style>
