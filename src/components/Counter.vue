<script>
  export default{
    data:() => {
      return {
        message:"Counter",
        count:0
      }
    },//data
    methods:{
      clearConsole:() => {console.clear();},
      //incCount(){this.count++;},
      incCount: function(){this.count++},
      decCount: function(){
        if (this.count > 0)
          this.count = this.count - 1
      },
      zerCount: function(){this.count = 0;}
    },//methods
    computed:{
      greeting: function(){
        console.log("greeting()")
        if(this.count === 0){
          this.message = "Please use buttons below to use counter";
          return this.message;
        }
        else {
          return "Count = " + this.count;
        }
      }//greeting
    }//computed
   
  }//export
</script>

<template>
  <p>Counter</p>
  <p>{{greeting}}</p>
  <button @click="clearConsole">Clear Console</button>
  <br>
  <button @click="incCount">+</button>
  <button @click="decCount">-</button>
  <button @click="zerCount">R</button>
</template>

<style>

</style>