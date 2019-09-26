<template>
  <div>
    <button class="block h-10 w-10 overflow-hidden rounded-full border-2 border-gray-600 focus:outline-none focus:border-white">
      <img
        class="h-full w-full object-cover"
        src="https://images.unsplash.com/photo-1487412720507-e7ab37603c6f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=256&q=80"
        alt="Your avatar"
        >
    </button>
    <div class="mt-2 bg-white rounded-lg w-48 py-2 shadow-xl">
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
</template>

<script>
export default {
}
</script>
