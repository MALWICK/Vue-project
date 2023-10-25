<template>
  <div>
    <input type="text" v-model="searchQuery" placeholder="Search" />
    <!-- Display the filtered items -->
    <ul>
      <li v-for="item in filteredItems" :key="item.apptitle">
        {{ item.apptitle }}
      </li>
    </ul>
  </div>
</template>

<script>
import { useDebouncedRef } from './debounce.js'

export default {
  data() {
    return {
      searchQuery: ''
    }
  },
  computed: {
    filteredItems() {
      const debouncedSearch = useDebouncedRef(this.searchQuery, 300)

      return this.items.filter(item => {
        // Perform your filtering logic here based on the debounced search query
        return item.apptitle.toLowerCase().includes(debouncedSearch.value.toLowerCase())
      })
    }
  },
  // Add your items array here
}
</script>