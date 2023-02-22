<script>
import RegisterCard from '../components/RegisterForm/RegisterCard.vue';
import Navbar from '../components/Navbar/Navbar.vue';
import RegisterStep from '../components/RegisterForm/RegisterStep.vue';
export default {
  components: {
    RegisterCard,
    Navbar,
    RegisterStep
  },
};
</script>

<template>
  <Navbar />
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content flex-col lg:flex-row-reverse">
      <RegisterStep />
      <RegisterCard />
    </div>
  </div>
</template>