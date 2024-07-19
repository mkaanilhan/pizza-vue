<script>

import { usePizzaStore } from '../stores/pizza.js'

export default {

    data() {

        return {

            store: usePizzaStore()
        }
    }
}

</script>


<template>


    <div class='bg-blue-700 text-white text-2xl p-4 flex justify-between'>



        <div> SU Pizza</div>

        <RouterLink to='/basket' class='underline cursor-pointer'> Basket: {{ store.numberOfItems }}</RouterLink>





    </div>


</template>