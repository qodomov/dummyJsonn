<template>
  <section class="products flex flex-col flex-grow py-5">
    <div class="container flex flex-col flex-grow mx-auto">
      <form class="mb-5 flex justify-center">
        <input
          type="text"
          v-model="state.search"
          class="border rounded outline-none focus:border-blue-300 py-2 px-5 w-full md:w-[50%]"
          placeholder="Search Products Using Title"
        />
      </form>
      <!-- Products FlexBox -->
      <div class="relative flex flex-col flex-grow">
        <!-- Loading -->
        <div class="flex flex-col justify-between flex-grow gap-2">
        
          <div class="flex flex-wrap flex-grow gap-6">
            <ProductCard 
            v-for="(product, index) in state.filterProducts"
            :key="index"
            :product="product" />
          </div>
          <Pagination :totalPages="state.totalPage" :handleClickPageNumber="state.handlePaginationNumber" />
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
// Components
import { onMounted } from 'vue';
import { ProductCard, Pagination } from '../../components'
import useProducts from '../../stores/products';
const state = useProducts()
onMounted(() => state.fetchProducts())

</script>
