<script>
import LoginCard from '../components/LoginForm/LoginCard.vue';
import Welcome from '../components/LoginForm/Welcome.vue';
import Navbar from '../components/Navbar/Navbar.vue';
export default {
  components: {
    LoginCard,
    Welcome,
    Navbar,
  },
};
</script>

<template>
  <Navbar />
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content flex-col lg:flex-row-reverse">
      <Welcome />

      <LoginCard />
    </div>
  </div>
</template>
