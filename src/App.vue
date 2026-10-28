<template>
  <div class="container">
    <h1 class="title">{{ title }}</h1>
  <Contact name="Samnang" :phone="15324229" :ownername="contactOwner"></Contact>
  <ButtonCounter></ButtonCounter>
  </div>
</template>
<script setup>
import Contact from './components/Contact.vue';
import ButtonCounter from './components/ButtonCounter.vue';

const title = 'Hello, World!'
const contactOwner = 'John'
</script>

<style scoped>
.title {
  color: green;
}
</style>