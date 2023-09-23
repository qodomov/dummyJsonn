<template>
  <!--User Card -->
  <figure class="product__card border self-start rounded-md relative">
    <h5 class="absolute bg-blue-500 right-0 text-xs p-2 rounded-bl text-white capitalize">Male</h5>
    <img
      class="w-full h-56 object-cover rounded-full"
      src="https://robohash.org/aliquamcumqueiure.png"
      alt=""
    />
    <figcaption class="h-[150px] p-2 pt-5 flex flex-col gap-2">
      <div class="flex justify-between gap-2">
        <p class="w-[50%] overflow-hidden text-ellipsis whitespace-nowrap">FirstName: Sheldon</p>
        <p class="w-[50%] overflow-hidden text-ellipsis whitespace-nowrap">LastName: Quigley</p>
      </div>
      <div class="flex justify-between gap-2">
        <p class="w-[50%] overflow-hidden text-ellipsis whitespace-nowrap">Email:jtreleven5@nhs.</p>
        <p class="w-[50%] overflow-hidden text-ellipsis whitespace-nowrap">Phone:+351 527 735</p>
      </div>

      <div class="flex justify-between gap-2">
        <p class="w-[50%] overflow-hidden text-ellipsis whitespace-nowrap">Age:30</p>
        <p class="w-[50%] overflow-hidden text-ellipsis whitespace-nowrap">UserName:jtreleven5</p>
      </div>
      <div class="flex flex-col absolute top-2 gap-2">
        <router-link
          class="bg-green-500 p-2 px-3 text-xs text-white rounded hover:bg-green-600 transition-all duration-300"
          :to="'/user/' + 1"
        >
          <i class="fa-solid fa-pen-to-square"></i>
        </router-link>
        <button
          type="button"
          class="bg-red-500 p-2 px-3 text-xs text-white rounded hover:bg-red-600 transition-all duration-300"
        >
          <i class="fa-solid fa-trash"></i>
        </button>
      </div>
    </figcaption>
  </figure>
</template>
<script setup></script>
