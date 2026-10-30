<template>
  <div class="bg-info rounded p-1 m-3">
    <div class="row">
      <div class="col-12">
        <h3>Name : {{ name }}</h3>
    <p>Email : {{ email }}</p>
    <p>Phone : {{ phone }}</p>
    <p class="float-end small" v-if="ownername != ''">
      *This contact info belong to {{ ownername }} *
    </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, defineProps } from 'vue';

// const email = ref('samnangjohn@gmail.com');
const props = defineProps({
  name: { type: String, required : true },
  phone: [String, Number],
  ownername: String,
  email : { type : String, required : false, default : "-n/a-"},
  isFavourite : Boolean
});
//props
</script>