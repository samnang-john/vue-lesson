<template>
  <div class="bg-info rounded p-2 m-2">
    <h3>Name : {{ name }}</h3>
    <p>Email : {{ email }}</p>
    <p>Phone : {{ phone }}</p>
    <p class="float-end small" v-if="ownername != ''">
      *This contact info belong to {{ ownername }} *
    </p>
  </div>
</template>

<script setup>
import { ref, defineProps } from 'vue';

// const email = ref('samnangjohn@gmail.com');
const props = defineProps({
  name: { type: String, required : true },
  phone: Number,
  ownername: String,
  email : { type : String, required : false, default : "-n/a-"}
});
//props
</script>