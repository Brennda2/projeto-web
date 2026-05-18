<template>
  <div class="flex flex-col p-5 bg-[#6F533A] min-h-screen">
    
    <div class="w-full overflow-hidden whitespace-nowrap mb-10 bg-[#543d2a] py-3 rounded-lg shadow-inner">
      
      <div class="inline-block animate-marquee space-x-10">
        
        <span class="text-xl md:text-2xl font-bold text-amber-200">
          Seja Bem-vindo!
        </span>
        
        <span class="text-amber-300 font-bold"></span>
        
        <span class="text-lg font-bold text-amber-100">
          Conheça nossos produtos!
        </span>
        <span class="text-lg font-bold text-amber-100">
          Projeto desenvolvido durante o Minicurso de Desenvolvimento Web!
        </span>
        
      </div>
    </div>
    
    <p v-if="loading" class="text-center text-white">Carregando...</p>
    
<div v-else class="w-full grid grid-cols-1 md:grid-cols-3 gap-8 justify-items-center max-w-5xl mx-auto">
      <ProductCard
        v-for="product in products"
        :key="product.id"
        :product="product"
      />
    </div>
    

    <div class="mt-12 flex justify-center items-center gap-6 text-white"> 
      <button 
        @click="prevPage" 
        :disabled="page === 1"
        class="px-4 py-2 bg-gray-700 rounded-lg disabled:opacity-30 hover:bg-gray-600 transition"
      >
        Anterior
      </button>
      
      <span class="font-medium text-lg">Página {{ page }} de {{ totalPages }}</span>
      
      <button 
        @click="nextPage" 
        :disabled="page === totalPages"
        class="px-4 py-2 bg-gray-700 rounded-lg disabled:opacity-30 hover:bg-gray-600 transition"
      >
        Próxima
      </button>   
    </div>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import { useProducts } from '../composables/useProducts'
import ProductCard from './ProductCard.vue'

const { products, loading, page, totalPages, fetchProducts, prevPage, nextPage } = useProducts()

onMounted(() => {
    fetchProducts()
})

</script>
