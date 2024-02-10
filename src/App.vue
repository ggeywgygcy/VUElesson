<template>
  <div class="container">
  <h1> Тест Emit и Provide</h1>
    <Card/>
    <div class="rows">
      <button v-on:click="addAnimal" type="button" class="btn btn-link">Link</button>
    </div>
  </div>
</template>

<script>
import Card from './components/card.vue'

export default {
  name: 'App',
  components: {
    Card
  },
  provide:{
    animal: "elephant"
  },
  methods:{
    addAnimals(){
      this.animal = this.animal + " " + this.animal
    }
  }
}
</script>

<style>

</style>
