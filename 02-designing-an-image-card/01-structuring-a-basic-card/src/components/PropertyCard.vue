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
      <div class="mt-2 flex items-center">
        <svg v-for="i in 5" :key="i" :class="i <= property.rating ? 'text-teal-500' : 'text-gray-400'" class="h-4 w-4 fill-current" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M8.133 20.333c-1.147.628-2.488-.387-2.269-1.718l.739-4.488-3.13-3.178c-.927-.943-.415-2.585.867-2.78l4.324-.654 1.934-4.083a1.536 1.536 0 0 1 2.804 0l1.934 4.083 4.324.655c1.282.194 1.794 1.836.866 2.78l-3.129 3.177.739 4.488c.219 1.331-1.122 2.346-2.269 1.718L12 18.214l-3.867 2.119z" fill-rule="evenodd"/>
        </svg>
        <span class="ml-2 text-gray-600 text-sm">{{ property.reviewCount }} reviews</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['property'],
}
</script>
