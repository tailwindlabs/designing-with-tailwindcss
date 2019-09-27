<template>
  <div class="relative">
    <button @click="isOpen = !isOpen" class="relative z-10 block focus:outline-none focus:border-white">
      <img
        class="h-8 w-8 overflow-hidden rounded-full border-2 border-gray-600 object-cover"
        src="https://images.unsplash.com/photo-1487412720507-e7ab37603c6f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=256&q=80"
        alt="Your avatar"
        >
    </button>
    <div v-if="isOpen" class="absolute right-0 mt-2">
      <button @click="isOpen = false" class="fixed inset-0 h-full w-full bg-black opacity-50 cursor-default" tabindex="-1"></button>
      <div class="relative z-10 bg-white rounded-lg w-48 py-2 shadow-xl">
        <a href="#account" class="block hover:text-white text-gray-800 px-4 py-2 hover:bg-indigo-500">
          Account settings
        </a>
        <a href="#support" class="block hover:text-white text-gray-800 mt-0 px-4 py-2 hover:bg-indigo-500">
          Support
        </a>
        <a href="#sign-out" class="block hover:text-white text-gray-800 mt-0 px-4 py-2 hover:bg-indigo-500">
          Sign out
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    }
  },
  created() {
    const handleEscape = (e) => {
      if (e.key === 'Esc' || e.key === 'Escape') {
        this.isOpen = false
      }
    }

    document.addEventListener('keydown', handleEscape)

    this.$once('hook:beforeDestroy', () => {
      document.removeEventListener('keydown', handleEscape)
    })
  }
}
</script>
