<template>
  <img class="img" alt="Vue logo" src="./assets/logo.png" />
  <div class="content">
    <router-link to="/"> Home </router-link>
    <router-link to="/guide"> Guide </router-link>
    <router-view v-slot="{ Component, route }">
      <transition
        :enter-active-class="route.meta.enterClass"
        :leave-active-class="route.meta.leaveClass"
      >
        <component :is="Component" />
      </transition>
    </router-view>
  </div>
</template>

<script setup>
// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 40px;
  text-align: center;
}
.content {
  width: 40%;
  min-width: 500px;
  margin: 0 auto;
  position: relative;
  text-align: justify;
}
.page {
  position: absolute;
  top: 45px;
}

a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  margin-right: 1em;
}
a:hover,
a.router-link-active {
  border-bottom: 2px solid #3498db;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.fade-enter-avtive,
.fade-leave-active {
  transition: opacity 0.5s ease-out;
}
</style>
