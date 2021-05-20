<template>
  <div class="home">
    home
  </div>
  <p>My name is {{ name }} and my age is {{ age }}</p>
  <button @click="handleClick">click me</button>
  <input type="text" v-model="name">
  <button @click="age++">add 1 to age</button>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Home',
  setup() {
    const name = ref('mario')
    const age = ref(30)    

    
    const handleClick = () => {
      name.value = 'luigi'
      age.value = 35
    }

    return { name, age, handleClick }
    
  }
}
</script>
