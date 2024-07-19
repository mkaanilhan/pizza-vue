<script>

import { usePizzaStore } from '../stores/pizza.js'
import BasketRow from '../components/BasketRow.vue'

export default {
    components: { BasketRow },

    data() {
        return {

            store: usePizzaStore()

        }
    }
}

</script>

<template>

    <div class='flex justify-between m-8'>
        <RouterLink to='/'>

            Back
        </RouterLink>

        <div>

            Total price: {{ store.sum.toFixed(2) }} $


        </div>
    </div>

    <div v-for='(pizza, index) in store.basketList' :key='index'>

        <BasketRow :item='pizza' />
    </div>

</template>