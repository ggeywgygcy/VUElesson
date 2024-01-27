<template>
  <div class="rows">
    <form class="row g-3">
      <div class="col-auto">
        <label for="inputName" class="visually-hidden">nAME</label>
        <input v-model="part" type="text" class="form-control" id="inputPassword2" placeholder="Название">
      </div>
      <div class="col-auto">
        <label for="inputPrace" class="visually-hidden">Цена за штуку</label>
        <input v-model="price" type="text" class="form-control" id="inputPassword2" placeholder="Цена за шт">
      </div>
      <div class="col-auto">
        <label for="inputVolume" class="visually-hidden">Количество</label>
        <input v-model="volume" type="text" class="form-control" id="inputPassword2" placeholder="Кол-во">
      </div>
      <div class="col-auto">
        <button v-on:click="added" class="btn btn-primary mb-3">Добавить</button>
      </div>
      <div class="col-auto">
        <button v-on:click="show" class="btn btn-primary mb-3">Посмотреть результат</button>
      </div>

      <div v-if="true" class="row">
        <ul id="array-rendering">
        <li v-for="item in product" :key="item.Pname" >
          {{ item.Pname }} {{ item.PRace }} {{ item.PVolume }} <br/>
        </li>
      </ul>
      </div>

      <div v-if="true" class="row">
        <ul id="array-rendering">
        <li v-for="item in test" :key="item" >
        </li>
      </ul>
      </div>

    </form>


  </div>
</template>

<script>
/* eslint-disable */
import Product from '../Product.js'
export default {
  name: 'Card',
  props: {
    msg: String
  },
  data(){
    return{
      product: [],
      part : "",
      volume : 0,
      price  : 0,
      check  : false,
      test   :[1,2,3,4]
    }
  },
  methods:{
    added(){
      let p = new Product(this.part, this.price, this.volume);
      this.product.push(p);
      
    }
  },
  show(){
    this.check = true
    alert(product[0].Pname)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
