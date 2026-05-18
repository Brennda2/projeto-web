<template>
  <div class="bg-[#E8D8C3] rounded-2xl w-78 p-6 shadow-md border border-[#D4AF37] cursor-pointer transition-all duration-200 transform active:scale-95 hover:shadow-lg hover:bg-gray-50 flex flex-col items-center text-center">
    
    <div class="w-full h-48 overflow-hidden rounded-xl mb-4 bg-[#F5E6D3]">
      <img 
        :src="product.thumbnail" 
        :alt="product.title" 
        class="w-full h-full object-cover"
      >
    </div>

    <h2 class="text-xl font-bold !text-black mb-1">{{ product.title }}</h2>
    
    <p class="text-xs font-semibold text-[#8B6B4C] uppercase tracking-widest mb-4">
      {{ product.category }}
    </p>
    
    <div class="w-full pt-4 border-t border-gray-300 flex justify-between items-center">
      <span class="text-gray-900 text-lg font-bold">R$ {{ product.price.toFixed(2) }}</span>
      <span class="bg-yellow-100 text-yellow-700 px-3 py-1 rounded-full text-sm font-bold">
        ⭐ {{ product.rating }}
      </span>
    </div>
  </div>
</template>

<script setup>
defineProps({
  product: {
    type: Object,
    required: true,
  }
})
</script>