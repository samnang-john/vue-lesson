<template>
  <div class="container">
    <h1 class="title">{{ title }}</h1>
    <div class="my-3">
      Contact ownername: <input v-model="ownerName" />
    </div>
    <div class="row">
      <div class="col-12" v-for="contact in contacts" :key="contact.name">
        <Contact :name="contact.name" :email="contact.email" :phone="contact.phone" :ownername="ownerName"></Contact>
      </div>
    </div>
    <ButtonCounter></ButtonCounter>
  </div>
</template>
<script setup>
import { ref, reactive } from 'vue';
import Contact from './components/Contact.vue';
import ButtonCounter from './components/ButtonCounter.vue';

const title = 'Hello, World!';
const ownerName = ref('John');
const contacts = reactive([
  {
    name: "Samnang",
    phone: "123456789",
    email: "samnang@gmail.com",
    ownerName: ownerName,
    isFavourite: false,
  },
  {
    name: "SreyNeang",
    phone: "123456789",
    email: "sreyneang@gmail.com",
    ownerName: ownerName,
    isFavourite: true,
  },
  {
    name: "Sokchea",
    phone: "123456789",
    email: "sokchea@gmail.com",
    ownerName: ownerName,
    isFavourite: false,
  }
]);
</script>

<style scoped>
.title {
  color: green;
}
</style>