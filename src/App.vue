

<template>
  <h1>{{ message }}</h1>
  <food-item 
  food-name="Apples"
  food-desc="apples can come in red and green"
  v-bind:is-favorite="true"/>
  <food-item
   food-name="Pizza" 
   food-desc="apples can come in red and green"
   v-bind:is-favorite="false"/>
  <food-item 
  food-name="Rice" 
  food-desc="apples can come in red and green"
  v-bind:is-favorite="false"/>
</template>

<script >
export default{
  data(){
    return{
      message: 'This is some text'
    }
  }
}

</script>
<style >
 #app > div {
    border: dashed black 1px;
    display: inline-block;
    width: 120px;
    margin: 10px;
    padding: 10px;
    background-color: lightgreen;
  }
</style>
