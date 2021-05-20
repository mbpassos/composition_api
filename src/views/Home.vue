<template>
  <div class="home">
    home
  </div>
  <h2>Refs</h2>
  <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
  <button @click="updateNinjaOne">Update Ninja One</button> 
  <h2>Reactive</h2>
  <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }}</p>
  <button @click="updateNinjaTwo">Update Ninja Two</button>
</template>

<script>
import { reactive, ref } from 'vue'
export default {
  name: 'Home',
  setup() {
    const ninjaOne = ref({ name: 'mario', age: 30 })
    const ninjaTwo = reactive({ name: 'luigi', age: 35 })

    const updateNinjaOne = () => {
      ninjaOne.value.age = 40
    }

    const updateNinjaTwo = () => {
      ninjaTwo.age = 45
    }

    return { ninjaOne, updateNinjaOne, ninjaTwo, updateNinjaTwo }
    
  }
}
</script>
