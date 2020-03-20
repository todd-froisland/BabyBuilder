<template>
  <div class="wrapper">
    <div class = "cartTitle">
    <h1>Cart-A-Babies</h1>
  </div>
  <div class = "cartABabies">
    <h1 v-if="this.$root.$data.cartSize ===  0"> Empty!</h1>
  <BabyList :BabyList="list"/>
</div>
  </div>
</template>

<script>
import BabyList from "../components/cartList.vue"
export default {
  name: 'Store',
  components: {
    BabyList
  },
  computed: {
    list() {
      return this.$root.$data.cart
    }
  },
}
</script>
<style scoped>
.cartTitle{
  background-color: #FFC79C;
font-family: 'Liu Jian Mao Cao', cursive;
padding: 50px;
font-size: 20px;

}
.cartABabies {
  background-color: #FF9C96;
  padding-top: 400px;
  padding-bottom: 400px;
  font-family: 'Liu Jian Mao Cao', cursive;
  font-size: 30px;
}
</style>
