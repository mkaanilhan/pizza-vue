<script>

import { usePizzaStore } from '../stores/pizza.js'

export default {

    data() {

        return {

            store: usePizzaStore()
        }
    },

    props: ['item']
}

</script>

<template>

    <div class='flex border border-black p-4 gap-4 justify-between'>


        <div class='flex gap-4'>

            <div>
                {{ item.name }}
            </div>

            <div>
                {{ item.price }} $
            </div>

        </div>



        <button @click='store.remove(item)'>Remove</button>



    </div>



</template>