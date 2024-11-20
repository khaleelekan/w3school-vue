<template>
    <div @:click="increment">
        <h2>{{ foodName }}</h2>
        <h2>{{ foodDesc }}</h2>
    </div>
    
</template>

<script>


export default{
    props:[
        'foodName','foodDesc'
    ],
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