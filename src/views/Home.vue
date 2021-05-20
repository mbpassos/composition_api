<template>
  <div class="home">
    home
  </div>
  <p>My name is {{ name }} and my age is {{ age }}</p>
  <button @click="handleClick">click me</button>
</template>

<script>
export default {
  name: 'Home',
  setup() {
    let name = 'mario'
    let age = 30

    const handleClick = () => {
      console.log('you clicked me')
    }

    return { name, age, handleClick }
    
  }
}
</script>
