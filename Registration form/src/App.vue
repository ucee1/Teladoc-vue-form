<template>
  <div class="app">
    <Header />
    <RegistrationForm />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import RegistrationForm from './components/RegistrationForm.vue';
import Footer from './components/Footer.vue';


export default {
  components: {
    Header,
    RegistrationForm,
    Footer,
  },
};
</script>
