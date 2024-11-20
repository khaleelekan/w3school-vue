<template>
    <div @:click="increment">
        <h2>{{ name }}</h2>
        <p>{{ message }}</p>
        <div id="red">{{ count }}</div>
    </div>
    
</template>

<script>


export default{
    data(){
        return{
            name: 'Apples',
            message: 'I like apples',
            count: 0
        }
    },
    methods:{
        increment(){
            this.count++;
        }
    }
}
</script>

<style>
 #red {
    font-weight: bold ;
    color: rgb(144, 12, 12);
  }</style>