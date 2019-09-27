<template>
  <div id="app" class="antialiased text-gray-900">
    <div class="bg-gray-800 min-h-screen py-32 px-6">
      <AccountDropdown/>
    </div>
  </div>
</template>

<script>
import AccountDropdown from './components/AccountDropdown'

export default {
  name: 'app',
  components: {
    AccountDropdown
  },
}
</script>

<style src="./assets/tailwind.css"></style>
