<template>
    <div @:click="increment">
        <h2>{{ foodName }}</h2>
        <h2>{{ foodDesc }}</h2>
        <img v-show="isFavorite" src="https://images.unsplash.com/photo-1511690656952-34342bb7c2f2?q=80&w=928&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="">
    </div>
    
</template>

<script>
import { type } from 'os';



export default{
    props:{
        foodName:{
            type: String,
            required: true,
        },
        foodDesc:{
            type: String,
            required: false,
            default: 'this is a default fooddesc',
            validator: function(){
                if (20 < value.length && value.length < 50){
                    return true
                }else{
                    return false
                }
            }
        },
        isFavorite:{
            type: Boolean,
            required: false,
            default: false

        }
    },
    data(){
        return{
           foodIsFavorite: this.isFavorite
        }
    },
    methods:{
        toggleFavorite(){
            this.foodIsFavorite = !this.foodIsFavorite
        }
    }
}
</script>

<style>
 #red {
    font-weight: bold ;
    color: rgb(144, 12, 12);
  }
  img{
    width: 80%;
    height: 80%;
  }
  </style>