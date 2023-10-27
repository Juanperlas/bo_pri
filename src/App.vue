<template>
  <h1 class="m-5 font-bold text-2xl">
    Vue 3 - Display a list of items with v-for
  </h1>

  <div class="w-12/12 border-2 border-black rounded-md ml-5 mr-5">
    <div class="flex justify-center">
      <div
        class="w-7/12 border-2 m-0.5 border-black rounded-full bg-yellow-400 font-extrabold"
      >
        Name
      </div>
      <div
        class="w-3/12 border-2 m-0.5 border-black rounded-full bg-yellow-400 font-extrabold"
      >
        Email
      </div>
      <div
        class="w-2/12 border-2 m-0.5 border-black rounded-full bg-yellow-400 font-extrabold"
      >
        Role
      </div>
    </div>

    <div class="flex justify-center" v-for="user in users" :key="user.email">
      <div
        class="w-7/12 border-2 m-0.5 border-black rounded-full bg-amber-100 font-medium"
      >
        {{ user.firstName }} {{ user.lastName }}
      </div>
      <div
        class="w-3/12 border-2 m-0.5 border-black rounded-full bg-amber-100 font-medium"
      >
        {{ user.email }}
      </div>
      <div
        class="w-2/12 border-2 m-0.5 border-black rounded-full bg-amber-100 font-medium"
      >
        {{ user.role }}
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const users = ref([
  {
    firstName: "Frank",
    lastName: "Murphy",
    email: "frank.murphy@test.com",
    role: "User",
  },
  {
    firstName: "Vic",
    lastName: "Reynolds",
    email: "vic.reynolds@test.com",
    role: "Admin",
  },
  {
    firstName: "Gina",
    lastName: "Jabowski",
    email: "gina.jabowski@test.com",
    role: "Admin",
  },
  {
    firstName: "Jessi",
    lastName: "Glacer",
    email: "jessi.glacer@test.com",
    role: "User",
  },
  {
    firstName: "Jay",
    lastName: "Bilzerian",
    email: "jay.bilzerian@test.com",
    role: "User",
  },
]);
</script>
