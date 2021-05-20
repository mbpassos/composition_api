<template>
  <div class="home">
    home
  </div>
  <p> {{ name }} </p>
</template>

<script>
import { computed } from 'vue'
export default {
  name: 'Home',
  setup() {
    const name = computed(() => {
      return 'shaun'
    })

    return { name }  
    
  }
}
</script>
