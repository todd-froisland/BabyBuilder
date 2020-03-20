<template>
  <div class="Home">
    <div class="body">
      <div class="body-object">
      <h1>Start Making Your Baby!</h1>
      <br><br>
      <p>Let's make some <strong>magic</strong> happen</p>
    <hr>
    <br>
    <p>Add a baby to add to your cart. Get as many as you'd like!</p>
    </div>
    <BabyList/>
    <div class="body-object">
      <p>More coming soon!</p>
    </div>
  </div>
    </div>
</template>

<script>
import BabyList from "@/components/BabyList.vue"
export default {
  name: 'Home',
  components: {
    BabyList
  },
  data() {
    return {
  }
},
}
</script>

<style scoped>
.body {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  background-color: #FF9C96;
  padding-top: 20px;
  padding-bottom: 20px;
}
 .body-object {
   display: flex;
   flex-direction: column;
   align-items: center;
   margin-top: 25px;
   font-size: 30px;
   margin-bottom: 25px;

   font-family: 'Liu Jian Mao Cao', cursive;

 }
 .body-object2 {
   align-items: center;
   display: flex;
   background-color:;
   height: 200px;
   width: 300px;
   margin: 10px;
   background-color: #D0D0D0;
   box-shadow: 0px 3px 5px gray;

   font-size: 50px;
   font-family: 'Liu Jian Mao Cao', cursive;
 }
 .body-object-2box {
   display: flex;
   flex-direction: row;
   justify-content: center;
   flex-wrap: wrap;
 }
</style>
