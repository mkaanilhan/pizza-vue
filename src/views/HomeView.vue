<script>

import PizzaCard from '../components/PizzaCard.vue'


export default {

  components: { PizzaCard },

  data() {
    return {

      baseUrl: 'https://669a57039ba098ed61ff463c.mockapi.io/api/v1/pizzas',
      pizzaList: []
    }
  },

  async created() {

    const response = await fetch(this.baseUrl)

    this.pizzaList = await response.json()

  }
}


</script>

<template>


  <main>


    <div v-for='(pizza, index) in pizzaList' class='p-4' :key='index'>


      <PizzaCard :pizzaProp='pizza' />



    </div>


  </main>
</template>
