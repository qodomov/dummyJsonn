<template>
  <!-- Product Update -->
  <section class="">
    <div class="container mx-auto font-roboto">
      <h2 class="text-center text-xl uppercase pt-10 pb-5">Update User</h2>
      <form @submit.prevent="handleSubmit" class="w-1/2 mx-auto flex flex-col gap-3">
        <input
          v-model="user.firstName"
          type="text"
          class="border w-full rounded p-2 px-5 outline-none"
          placeholder="FirstName"
        />
        <input
          v-model="user.lastName"
          type="text"
          class="border w-full rounded p-2 px-5 outline-none"
          placeholder="LastName"
        />
        <input
          v-model="user.email"
          type="text"
          class="border w-full rounded p-2 px-5 outline-none"
          placeholder="Email"
        />
        <input
          v-model="user.username"
          type="text"
          class="border w-full rounded p-2 px-5 outline-none"
          placeholder="Username"
        />
        <input
          v-model="user.age"
          type="number"
          class="border w-full rounded p-2 px-5 outline-none"
          placeholder="Age"
        />
        <input
          v-model="user.phone"
          type="text"
          class="border w-full rounded p-2 px-5 outline-none"
          placeholder="Phone"
        />
        <button
          type="submit"
          class="bg-green-500 self-end px-5 py-2 text-white rounded hover:bg-green-600 transition-all duration-300"
        >
          Update
        </button>
      </form>
    </div>
  </section>
</template>
<script setup>
import { reactive } from 'vue'
const user = reactive({
  firstName: '',
  lastName: '',
  email: '',
  age: '',
  phone: '',
  username: ''
})
const handleSubmit = async () => {
  try {
    //
  } catch (err) {
    console.log(err)
  }
}
</script>
