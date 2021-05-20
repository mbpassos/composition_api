<template>
  <div class="home">
    home
  </div>
  <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
  <button @click="handleClick">click me</button>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Home',
  setup() {
    let name = 'mario'
    let age = 30

    const p = ref(null)

    const handleClick = () => {
      console.log(p.value)
      p.value.classList.add('test')
      p.value.textContent = 'hello, ninjas'
    }

    return { name, age, handleClick, p }
    
  }
}
</script>
