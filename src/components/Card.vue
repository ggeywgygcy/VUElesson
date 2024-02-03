<template>
  <div class="rows">
    <slot>   </slot>

    <div class="row g-3">
      <div class="col-auto">
        <label for="inputName" class="visually-hidden">nAME</label>
        <input v-model="part.Pname" type="text" class="form-control" id="inputPassword2" placeholder="Название">
      </div>
      <div class="col-auto">
        <label for="inputPrace" class="visually-hidden">Цена за штуку</label>
        <input v-model="part.PRace" type="text" class="form-control" id="inputPassword2" placeholder="Цена за шт">
      </div>
      <div class="col-auto">
        <label for="inputVolume" class="visually-hidden">Количество</label>
        <input v-model="part.PVolume" type="text" class="form-control" id="inputPassword2" placeholder="Кол-во">
      </div>
      <div class="col-auto">
        <button v-on:click="added" class="btn btn-primary mb-3">Добавить</button>
      </div>
      <div class="col-auto">
        <button v-on:click="show" class="btn btn-primary mb-3">Посмотреть результат</button>
      </div>

      <slot>   </slot>

      <div v-if="true" class="row">
        <ul id="array-rendering">
        <li v-for="item in product" :key="item.Pname" >
          {{ item.Pname }} {{ item.PRace }} {{ item.PVolume }} <br/>
        </li>
      </ul>
      </div>

    </div>
    <div class="alert alert-dark" role="alert">
  У нас в корзине лежит товар весом больше 30ти киллограмитоод: {{resultSum}}
</div>

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
      part : Product,
      check  : false
    }
  },
  methods:{
    added(){
      this.product.push({...this.part});
      
    }
  },
  show(){
    this.check = !this.check
  },
  computed : {
    resultSum(){
     
      return this.product.length;
     }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
