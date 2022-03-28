<template>
  <div class="home">
    <div>
    <img src="../assets/robot-home.png" alt="robot" aria-hidden="true" class="robot">
    </div>
    <div class="get-started">
      <router-link to="/build">Get Started</router-link>
      building your first robot!
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.home{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
img{
  height: 600px;
}
</style>
