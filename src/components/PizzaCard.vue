<script>

import { usePizzaStore } from '../stores/pizza.js'

export default {

    data() {
        return {

            store: usePizzaStore()
        }
    },


    props: ['pizzaProp']

}



</script>


<template>


    <div class='border-2 border-black p-4'>

        <img :src="pizzaProp.img" class='w-full h-72 object-cover'>

        <div class='flex justify-between mt-4 items-center'>

            <div class='text-2xl'>{{ pizzaProp.name }}</div>

            <div class='italic'>{{ pizzaProp.price }}</div>

        </div>

        <div class='flex gap-4'>


            <div class='mt-4 cursor-pointer underline' @click='store.remove(pizzaProp)'>Remove</div>


            <div class='mt-4 cursor-pointer underline' @click='store.add(pizzaProp)'>Add</div>


        </div>



    </div>


</template>