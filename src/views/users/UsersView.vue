<template>
  <section class="users flex flex-col flex-grow py-5">
    <div class="container flex flex-col flex-grow mx-auto">
      <form class="mb-5 flex justify-center">
        <input
          type="text"
          class="border rounded outline-none focus:border-blue-300 py-2 px-5 w-full md:w-[50%]"
          placeholder="Search Users Using FirstName"
        />
      </form>
      <!-- Users FlexBox -->
      <div class="relative flex flex-col flex-grow">
        <!-- Loading -->
        <div class="flex flex-col flex-grow justify-between gap-2">
          <div class="flex flex-wrap gap-6">
            <UserCard />
          </div>
          <Pagination :totalPages="10" :handleClickPageNumber="() => {}" />
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
// Components
import { UserCard, Pagination } from '../../components'
</script>
