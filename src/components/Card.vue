<template>
  <div class="card">
    <div class="card" style="width: 18rem;">
      <img v-if="openImg" v-bind:src="foto" class="card-img-top" alt="...">
      <p class="card-text">{{msg}}</p>
      <p class="card-text">{{foto}}</p>
      <p class="card-text">{{disable}}</p>
  </div>
  <button v-on:click="remove" class="btn btn-primary">{{msgBtn}}</button>

</div>
</template>

<script>
/* eslint-disable */
export default {
  name: 'Card',
  props: {
    msg: String,
    foto: String,
    view: String
  },
  data() {
    return{
      openImg: true,
      msgBtn: "Ликвидировать"
    }
  },  

  methods:{
    remove(){
    this.openImg = !this.openImg;
    if(this.openImg){
      this.msgBtn = "Ликвидировать"
    }else{
      this.msgBtn = "Восстановить"
    }
    }
  }
}
</script>


<style scoped>

</style>
