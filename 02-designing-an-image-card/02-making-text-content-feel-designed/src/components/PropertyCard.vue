<template>
  <div class="bg-white border rounded-lg overflow-hidden">
    <img :src="property.imageUrl" :alt="property.imageAlt">
    <div class="p-6">
      <div class="text-gray-600 text-xs uppercase font-semibold tracking-wide">
        {{ property.beds }} beds &bull; {{ property.baths }} baths
      </div>
      <h4 class="font-semibold text-lg leading-tight truncate">{{ property.title }}</h4>
      <div class="mt-1">
        {{ property.formattedPrice }}
        <span class="text-gray-600 text-sm"> / wk</span>
      </div>
      <div class="mt-4">
        <span class="text-teal-600 font-semibold">{{ property.rating }}/5 stars</span>
        <span class="text-gray-600 text-sm"> (based on {{ property.reviewCount }} reviews)</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['property'],
}
</script>
