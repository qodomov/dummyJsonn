<template>
  <section class="posts flex flex-grow pt-2 pb-3">
    <div class="container mx-auto flex flex-col flex-grow">
      <div class="flex gap-5 md:flex-row flex-col-reverse flex-grow items-start mt-5">
        <!-- Posts -->
        <div class="flex flex-col flex-grow gap-3 w-full md:w-[80%]">
          <PostCard />
        </div>
        <!-- Tags -->
        <div class="bg-gray-100 p-3 rounded md:w-[15%] w-full">
          <h3 class="mb-3 text-xl font-medium">Tags</h3>
          <div class="flex flex-wrap gap-2">
            <p
              class="bg-gray-300 p-2 cursor-pointer rounded-full text-sm hover:bg-green-600 hover:text-white transition-all duration-200"
            >
              All
            </p>
            <!-- Tags  -->
            <p
              class="bg-gray-300 p-2 cursor-pointer rounded-full text-sm hover:bg-green-600 hover:text-white transition-all duration-200"
            ></p>
          </div>
        </div>
      </div>
      <Pagination :totalPages="10" class="mt-3" />
    </div>
  </section>
</template>
<script setup>
// Components
import { PostCard, Pagination } from '../../components'
</script>
