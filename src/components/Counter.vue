<script>
  export default{
    data:() => {
      return {
        name:"Special counter of peter"
      }
    },//data
    methods:{
      clearConsole:() => {console.clear();},
      debugObject: (event) => {
        console.log("debugObject");
        console.log(event);
      }//debugObject
    }//methods
  }//export
</script>

<template>
  <p>Counter</p>
  <p>{{name}}</p>
  <button @click="clearConsole">Clear Console</button>
  <button @click="debugObject($event)">DebugObject</button>
</template>

<style>

</style>