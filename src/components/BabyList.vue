<template>
  <div class = "wrapper">
      <div class ="baby" v-for="baby in babies" :key="baby.id">
        <div class ="babyName">
          <h1>{{baby.name}}</h1>
        </div>
        <div class="babyimage">
          <img :src="baby.image" height = "200px">
        </div>
        <div class ="buttonstuff">
        <button class="auto" v-on:click="addtoCart(baby)"><strong>Add to Cart</strong></button>
      </div>
    </div>
  </div>
</template>

<script>
 export default {
   name: 'BabyList',
  computed: {
    babies() {
      return this.$root.$data.babies;
    },
  },
    methods: {
     addtoCart(baby) {
      this.$root.$data.cart.push(baby);
      this.$root.$data.cartSize += 1;
     }
   }
 }
</script>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
.baby {
  flex-direction: column;
  align-items: center;
  display: flex;
  background-color:;
  height: 350px;
  width: 400px;
  margin: 50px;
  background-color: #D0D0D0;
  box-shadow: 0px 3px 5px gray;
  font-size: 50px;
  font-family: 'Liu Jian Mao Cao', cursive;
}
.babyName {
  margin-bottom: 5px;
  font-size: 15px;
  background-color: #FFB28A;
  padding: 5px;
  padding-left: 50px;
  padding-right: 50px;
}
.babyimage {
}

button {
  background-color: #FFB28A;
  font-size: 30px;
  border: none;
  font-family: 'Liu Jian Mao Cao', cursive;
  box-shadow: 0px 1px 5px gray;
  padding: 10px;
  margin-top: 15px;
  padding-bottom: 25px;
  border-radius: 10px;

}
</style>
